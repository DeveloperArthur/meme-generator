<template>
  <div id="app" align="center">
    <header>
      <h1>Meme Generator</h1>
    </header>
    <br>
    <div id="resultado" v-if="mostrarMeme1 || mostrarMeme2 || mostrarMeme3 || mostrarMeme4 || mostrarMeme5">
      {{ fraseEscolhida }}
      <br>
      <img v-if="mostrarMeme1" src="./img/meme1.png" width="500px" height="500px">
      <img v-if="mostrarMeme2" src="./img/meme2.png" width="500px" height="500px">
      <img v-if="mostrarMeme3" src="./img/meme3.png" width="500px" height="500px">
      <img v-if="mostrarMeme4" src="./img/meme4.png" width="500px" height="500px">
      <img v-if="mostrarMeme5" src="./img/meme5.png" width="500px" height="500px">
    </div>
    <br>
    <p>Selecione o Meme</p>
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
    
    <hr>
    <p>Escreva a frase do Meme</p>
    <input type="text" style="width: 400px; height: 30px;" v-model="fraseDoMeme">
    <hr>
    <button class="btn btn-primary" @click="escolher">Gerar meme</button>
    <br><br>
  </div>
</template>

<script>
export default {
  data(){
    return{
      memeSelecionado: '',
      fraseEscolhida: '',
      fraseDoMeme: '',
      mostrarMeme1: false,
      mostrarMeme2: false,
      mostrarMeme3: false,
      mostrarMeme4: false,
      mostrarMeme5: false
    }
  },
  methods:{
    escolher(){
      if(this.memeSelecionado == 'meme1'){
        this.mostrarMeme1 = true;
        this.mostrarMeme2 = false;
        this.mostrarMeme3 = false;
        this.mostrarMeme4 = false;
        this.mostrarMeme5 = false;
      }else if(this.memeSelecionado == 'meme2'){
        this.mostrarMeme2 = true;
        this.mostrarMeme1 = false;
        this.mostrarMeme3 = false;
        this.mostrarMeme4 = false;
        this.mostrarMeme5 = false;
      }else if(this.memeSelecionado == 'meme3'){
        this.mostrarMeme3 = true;
        this.mostrarMeme1 = false;
        this.mostrarMeme2 = false;
        this.mostrarMeme4 = false;
        this.mostrarMeme5 = false;
      }else if(this.memeSelecionado == 'meme4'){
        this.mostrarMeme4 = true;
        this.mostrarMeme1 = false;
        this.mostrarMeme2 = false;
        this.mostrarMeme3 = false;
        this.mostrarMeme5 = false;
      }else if(this.memeSelecionado == 'meme5'){
        this.mostrarMeme5 = true;
        this.mostrarMeme1 = false;
        this.mostrarMeme2 = false;
        this.mostrarMeme3 = false;
        this.mostrarMeme4 = false;
      }
      this.fraseEscolhida = this.fraseDoMeme;
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

#resultado{
  border:1px solid black;
  font-size: 30px;
  width: 550px;
  height: 550px;
  background-color: white;
}
</style>
