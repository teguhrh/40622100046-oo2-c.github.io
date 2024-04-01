<template>
  <h1>Hallo warga widit</h1>
  <br />
  <h1>coba pencet tombol dibawah : {{ count }}</h1>
  <br />
  <br />
  <button @click="increment">Tambahkan Angka</button>
  <br />
  <button @click="decrement">Kurangi Angka</button>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },

  methods: {
    increment() {
      this.count++
    },
    decrement() {
      if (this.count > -100) {
        this.count--
      }
    }
  },

  mounted() {
    console.log(`The initial count is ${this.count}.`)
  }
}
</script>
<style scoped>
button {
  margin-bottom: 10px; /* Menambahkan jarak 10px antara tombol */
}
</style>
