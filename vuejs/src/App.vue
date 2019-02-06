<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <router-link to="/Kelas">Data Kelas </router-link>
    <router-link to="/siswa">Data Siswa</router-link>
    <router-view/> -->
  <h1>{{ nama }}</h1>
  <h2>Nama : <input v-model="nama" type="" name=""><br></h2>
  <h2>Nilai Anda : {{  nilai }}</h2>
  <button @click = "totalnilai">Click Me</button>
  <h2>1. Siapakah nama pemeran utama film Spongebob ?</h2>
  <input type="radio" name="" v-model="soal1" value="Patrick">Patrick
  <input type="radio" name="" v-model="soal1" value="Sandy">Sandy
  <input type="radio" name="" v-model="soal1" value="Krab">Krab
  <input type="radio" name="" v-model="soal1" value="Spongebob">Spongebob<br>
  <h2>2. Siapakah nama guru PWD kelas XII ?</h2>
  <input type="radio" name="" v-model="soal2" value="fery">Pak Ferry
  <input type="radio" name="" v-model="soal2" value="ali">Pak Ali
  <input type="radio" name="" v-model="soal2" value="taufik">Pak Taufik
  <input type="radio" name="" v-model="soal2" value="arne">Bu Arne<br>
  <h2>3. Berapakah 1 + 2 ?</h2>
  <input type="radio" name="" v-model="soal3" value="1">1
  <input type="radio" name="" v-model="soal3" value="3">3
  <input type="radio" name="" v-model="soal3" value="5">5
  <input type="radio" name="" v-model="soal3" value="7">7<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'
*/

export default {
  name: 'App',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
    }
  },
  methods: {
    totalnilai(){
      if(this.soal1 == 'Spongebob' && this.soal2 == 'fery' && this.soal3 == '3') {
        this.nilai=+3
      }
      else if (this.soal1 == 'Spongebob' && this.soal2 == 'fery') {
        this.nilai=+2
      }
      else if (this.soal1 == 'Paris' && this.soal3 == '3') {
        this.nilai=+2
      }
      else if (this.soal2 == 'fery' && this.soal3 == '3') {
        this.niali=+2
      }
      else if (this.soal1 == 'Spongebob') {
        this.nilai=+1
      }
      else if (this.soal2 == 'fery') {
        this.nilai=+1
      }
      else if (this.soal3 == '3') {
        this.nilai=+1
      }
      else{
        this.nilai = 0
      }
    }
  }
  /*,
  components: {
    HelloWorld
  }*/
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
