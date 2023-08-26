<script setup>
  import Header from "./components/Header.vue";
  import { useRouter } from "vue-router";

  const router = useRouter();
</script>

<template>
  <div class="flex h-screen flex-col items-center justify-center">
    <div
      class="flex h-screen flex-col gap-5 p-5 md:max-w-[50%] lg:max-w-[50%] xl:max-w-[50%]">
      <Header
        :class="
          router.currentRoute.value.fullPath != '/' ? 'sticky top-5' : ''
        " />
      <router-view class=""></router-view>
    </div>
  </div>
</template>
