<template>
  <section>
    <img v-bind:src="picture" v-bind:width="size" v-bind:height="size" />
    <h3>{{ getFullName() }}</h3>
    <p>ที่อยู่ : <span v-html="address"></span></p>
    <a :href="social" target="_blank">facebook </a>

    <ul>
      <li>{{ hobby[0] }}</li>
      <li>{{ hobby[1] }}</li>
      <li>{{ hobby[2] }}</li>
    </ul>
    <p>ข้อมูลพื้นฐาน :</p>
    <ul>
      <li>เพศ : {{ general.gender }}</li>
      <li>ส่วนสูง {{ general.height }}</li>
      <li>สถานะ : {{ general.status }}</li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      firstName: "Yodfan",
      lastName: "Supit",
      age: 21,
      address: "<strong>1 สุขสวัสดิ์ 26 แยก 1</strong>",
      picture:
        "https://www.jollyboxdesign.com/wp-content/uploads/2021/08/Administrator.png",
      size: 150,
      social: "https://www.facebook.com/honniinana",
      hobby: ["ฟังเพลง", "เที่ยว", "เล่นเกมส์"],
      general: { gender: "ชาย", height: 180, status: false },
    };
  },
  methods: {
    getFullName() {
      return this.firstName + " " + this.lastName;

      // return `${this.firstName}  ${this.lastName}`;
    },
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
