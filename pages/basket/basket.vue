<template>
  <div class="cart">
    <h1>Корзина</h1>
    <ul>
      <li v-for="product in data" :key="product.id">
        <img :src="product.image" alt="product image" />
        <h2>{{ product.name }}</h2>
        <p>{{ product.price }}</p>
        <button @click="removeProduct(product)">Удалить</button>
      </li>
    </ul>
    <div class="total">
      <p>Итого: {{ data.totalPrice }}</p>
    </div>
    <button @click="checkout">Оформить заказ</button>
  </div>
</template>

<script>
import { createClient } from "@supabase/supabase-js";
const client = createClient(
  "https://nrdgebxynjkyfcrwohjo.supabase.co",
  "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im5yZGdlYnh5bmpreWZjcndvaGpvIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDE2ODc4NTYsImV4cCI6MjAxNzI2Mzg1Nn0.ML9-cPzQOD3BPeUMFq-4fqJZwL7D-KGz0EAhgzgDURk"
);
const { data } = await useAsyncData("bucket", async () => {
  const { data } = await client.from("bucket").select("*");
  return data;
});
console.log(data.value);
export default {
  data() {
    return {
      products: [],
      totalPrice: 0,
    };
  },
  mounted() {
    // Получить список товаров из корзины
    this.getProducts();
  },
  methods: {
    // Получить список товаров из корзины
    getProducts() {
      // Используем API Supabase для получения списка товаров из таблицы `cart`
      this.$supabase
        .from("cart")
        .select("id", "name", "price")
        .where({
          user_id: this.$auth.user().id,
        })
        .then((result) => {
          this.products = result.data;
          // Рассчитать общую стоимость товаров
          this.totalPrice = 0;
          for (const product of this.products) {
            this.totalPrice += product.price;
          }
        });
    },
    // Удалить товар из корзины
    removeProduct(product) {
      // Используем API Supabase для удаления товара из таблицы `cart`
      this.$supabase
        .delete("cart", {
          id: product.id,
          user_id: this.$auth.user().id,
        })
        .then(() => {
          // Обновить список товаров в корзине
          this.getProducts();
        });
    },
  },
};
</script>
