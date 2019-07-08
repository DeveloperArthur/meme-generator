<template>
  <div id="app" align="center">
    <header>
      <h1>Meme Generator</h1>
    </header>
    <br>
    <img v-if="mostrarMeme1" src="./img/meme1.png" width="500px" height="500px">
    <img v-if="mostrarMeme2" src="./img/meme2.png" width="500px" height="500px">
    <img v-if="mostrarMeme3" src="./img/meme3.png" width="500px" height="500px">
    <img v-if="mostrarMeme4" src="./img/meme4.png" width="500px" height="500px">
    <img v-if="mostrarMeme5" src="./img/meme5.png" width="500px" height="500px">
    <br>
    <tr>
      <td>
        <img src="./img/meme1.png" alt="meme1" width="100px" height="100px">
        <br>
        <input type="radio" name="meme" v-model="memeSelecionado" value="meme1">
      </td>
      <td>
        <img src="./img/meme2.png" alt="meme2" width="100px" height="100px">
        <br>
        <input type="radio" name="meme" v-model="memeSelecionado" value="meme2">
      </td>
      <td>
        <img src="./img/meme3.png" alt="meme3" width="100px" height="100px">
        <br>
        <input type="radio" name="meme" v-model="memeSelecionado" value="meme3">
      </td>
      <td>
        <img src="./img/meme4.png" alt="meme4" width="100px" height="100px">
        <br>
        <input type="radio" name="meme" v-model="memeSelecionado" value="meme4">
      </td>
      <td>
        <img src="./img/meme5.png" alt="meme5" width="100px" height="100px">
        <br>
        <input type="radio" name="meme" v-model="memeSelecionado" value="meme5">
      </td>
    </tr>
    <button class="btn btn-success" @click="escolher">Selecionar</button>
    <hr>
    <input type="text" style="width: 400px; height: 30px;" v-model="fraseDoMeme">
    <br>
    <button class="btn btn-primary">Gerar meme</button>
    <br><br>
  </div>
</template>

<script>
export default {
  data(){
    return{
      memeSelecionado: '',
      fraseDoMeme: ''
    }
  },
  methods:{
    escolher(){
      alert(this.memeSelecionado);
    }
  }
}
</script>

<style>
header{
  background: linear-gradient(purple, red);
  display: flex;
  flex-direction: column;
  color: black
}
body{
    background: linear-gradient(white, gray) no-repeat center center fixed;
    font-family: Helvetica, Arial, sans-serif;
    margin: 0;
}
p{
  font-size: 28px;
}
</style>
