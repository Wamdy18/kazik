<template>
  <div class="kazik-tablo-div">
    <div class="kazik-tablo">
      <kazik-item :item="items[0]" />
      <kazik-item :item="items[1]" />
      <kazik-item :item="items[2]" />
    </div>
    <div class="a1"><button class="kazik-roll-btn">Крутить</button></div>
  </div>
</template>

<script>
import KazikItem from './KazikItem.vue'
export default {
  components: { KazikItem },
  data() {
    return {
      items: [
        {
          id: 0,
          src: '/src/assets/img/crystal.png',
        },
        {
          id: 1,
          src: '/src/assets/img/money.png',
        },
        {
          id: 2,
          src: '/src/assets/img/banknote.png',
        },
      ],
    }
  },
}
</script>

<style></style>
