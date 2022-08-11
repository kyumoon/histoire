<script lang="ts" setup>
import lottie from "lottie-web";
import { onMounted, ref } from "vue";
import lottieData from "../lottie-data";

const el = ref(null as null | HTMLElement);

onMounted(() => {
  const animData = {
    container: el.value as HTMLElement,
    animType: "svg",
    loop: true,
    prerender: true,
    autoplay: true,
    data: lottieData,
  };
  lottie.loadAnimation(animData);
});
</script>

<template>
  <Story title="Lottie Test">
    <Variant title="default">
      Lottie Test!
      <div ref="el"></div>
    </Variant>
  </Story>
</template>
