<template>
  <div class="flex mt-0">
    <div class="w-14 bg-slate-100 text-center flex flex-col px-1 gap-1">
      <div class="tooltip tooltip-right" data-tip="hello" v-for="i in 4" :key="i">
        <button href="" class="rounded-lg btn btn-ghost px-2 w-full">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 640 512"
            class="w-6"
          >
            <path
              d="M320 384H128V224H64v256a32 32 0 0 0 32 32h256a32 32 0 0 0 32-32V224h-64zm192-160v272a16 16 0 0 0 16 16h32a16 16 0 0 0 16-16V224z"
              class="fa-secondary"
            />
            <path
              d="M634.55 142.2c14.1 21.3-1.1 49.8-26.6 49.8H32.05c-25.6 0-40.8-28.5-26.6-49.8l85.3-128A31.87 31.87 0 0 1 117.35 0h405.2a32.18 32.18 0 0 1 26.7 14.2z"
              fill="#dc2626"
            />
          </svg>
        </button>
      </div>
    </div>
    <ul class="menu bg-base-100 w-56 p-2 rounded-box">
      <li class="menu-title">
        <span>ໝວດໝູ່ສິນຄ້າ</span>
      </li>
      <li><a>Item 1</a></li>
      <li><a>Item 2</a></li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>