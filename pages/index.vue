<script setup>
definePageMeta({
  title: "Dashboard",
});
const perpage = ref("1");
</script>
<template>
  <div>
    <TablePanel :numpage="1" v-model:totalPage="perpage" title="ຜູ້ໃຊ້ລະບົບ">
      <template #action>
        <label for="my-modal" class="btn btn-square btn-sm btn-primary ml-2"
          >+</label
        >
      </template>
      <template #search>
        <div class="flex">
          <select
            class="select select-sm bg-base-200 rounded-l-lg rounded-r-none"
          >
            <option value="cust_id">ລະຫັດ</option>
            <option value="fullname">ຊື່ ແລະ ນາມສະກຸນ</option>
            <option value="mobile">ເບີໂທ</option>
          </select>
          <input
            type="text"
            class="input w-full input-sm max-w-xs transparent rounded-none"
            placeholder="ປ້ອນການຄົ້ນຫາ..."
          />

          <button
            type="button"
            class="rounded-r-lg rounded-l-none btn-sm btn px-3"
          >
            ຄົ້ນຫາ
          </button>
        </div>
      </template>
      <template #body> </template>
    </TablePanel>
  </div>
</template>