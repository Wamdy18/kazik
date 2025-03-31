<template>
  <div class="kazik-item">
    <img :src="item.src" alt="" />
  </div>
</template>

<script>
export default {
  props: {
    item: {
      default: {
        src: '',
      },
    },
  },
}
</script>

<style></style>
