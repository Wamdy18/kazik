<template>
  <div class="kazik-tablo-div">
    <div class="kazik-score">Денег: {{ currentMoney }}</div>
    <div class="kazik-tablo">
      <kazik-item :item="items[0]" />
      <kazik-item :item="items[1]" />
      <kazik-item :item="items[2]" />
    </div>
    <div class="a1"><button class="kazik-roll-btn" @click="rollKazik">Крутить</button></div>
  </div>
</template>

<script>
import KazikItem from './KazikItem.vue'
export default {
  components: { KazikItem },
  data() {
    return {
      currentMoney: 500,
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
  methods: {
    rollKazik() {
      const a = Math.floor(Math.random() * 3) // от 0 до 3
      console.log(a)
      switch (a) {
        case 0:
          this.items[0].src = '/src/assets/img/crystal.png'
          break
        case 1:
          this.items[0].src = '/src/assets/img/money.png'
          break

        case 2:
          this.items[0].src = '/src/assets/img/banknote.png'
          break

        default:
          break
      }
      const b = Math.floor(Math.random() * 3) // от 0 до 3
      switch (b) {
        case 0:
          this.items[1].src = '/src/assets/img/crystal.png'
          break
        case 1:
          this.items[1].src = '/src/assets/img/money.png'
          break

        case 2:
          this.items[1].src = '/src/assets/img/banknote.png'
          break

        default:
          break
      }
      const c = Math.floor(Math.random() * 3) // от 0 до 3
      switch (c) {
        case 0:
          this.items[2].src = '/src/assets/img/crystal.png'
          break
        case 1:
          this.items[2].src = '/src/assets/img/money.png'
          break

        case 2:
          this.items[2].src = '/src/assets/img/banknote.png'
          break

        default:
          break
      }

      if (a == b && b == c) {
        this.currentMoney += 100
      } else {
        this.currentMoney -= 10
      }
    },
  },
}
</script>

<style></style>
