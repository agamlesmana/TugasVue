<template>
  <div>
    <h1>{{ nama }}</h1>
    <input type="text" v-model="nama">
    <br><br>
    Nilai Anda : {{ nilai }}
    <br>    
    <h2>{{ soal1 }}</h2>
    <input type="radio" name="jawaban1" :disabled="checked" @click="benar"> Susilo Bambang Yudhoyono
    <input type="radio" name="jawaban1" :disabled="checked" > Sisilo Bambang Yaris
    <input type="radio" name="jawaban1" :disabled="checked"> Susilo Bopung Yandi
    <h2>{{ soal2 }}</h2>
    <input type="radio" name="jawaban2" :disabled="checked2"> hidung
    <input type="radio" name="jawaban2" :disabled="checked2"> telinga
    <input type="radio" name="jawaban2" :disabled="checked2" @click="benar2"> Insang
    <h2>{{ soal3 }}</h2>
    <input type="radio" name="jawaban3" :disabled="checked3" @click="benar3"> 24
    <input type="radio" name="jawaban3" :disabled="checked3" > 25
    <input type="radio" name="jawaban3" :disabled="checked3"> 23
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      nama: 'Nama Anda',
      nilai: 0,
      soal1: '1. Siapa nama lengkap SBY ?',
      soal2: '2. Ikan bernafas menggunakan ?',
      soal3: '3. Ada berapa total huruf hijaiyah" adalah......'
    }
  },
  methods:{
    benar(){
      this.nilai += 1,
      this.checked = true
    },
     benar2(){
      this.nilai += 1,
      this.checked2 = true
    },
     benar3(){
      this.nilai += 1,
      this.checked3 = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  font-size: 30px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
