<script setup>
definePageMeta({
  title: "Dashboard",
});
const perpage = ref("1");
</script>
<template>
  <div class="w-full">
    <section>
      <h1>ສິນຄ້າມາໃໝ່</h1>
      <CarProductgrid />
    </section>
    <section>
      <h1>ສິນຄ້າມາໃໝ່</h1>
      <div class="grid grid-cols-7 gap-4">
        <CardProduct v-for="i in 20" :key="i" />
      </div>
    </section>
  </div>
</template>