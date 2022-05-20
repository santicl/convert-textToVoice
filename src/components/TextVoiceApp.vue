<template>
  <div class="container-all">
    <div class="container-logo">
      <img src="./assets/S.png" alt="" />
      <button class="btn">
        <strong>TextVoice</strong
        ><i class="fa fa-microphone" aria-hidden="true"></i>
      </button>
    </div>
    <textarea
      type="text"
      id="textArea"
      rows="8"
      placeholder="Ingresa lo que desees escuchar"
    ></textarea>
    <div class="container-btn">
      <button class="btn-play" @click="speakInputText">
        Reproducir<i class="fa fa-microphone" aria-hidden="true"></i>
      </button>
      <button class="btn-stop" @click="stopText">
        Detener<i class="fa fa-stop-circle-o" aria-hidden="true"></i>
      </button>
    </div>
  </div>
</template>

<script>
var speech = new SpeechSynthesisUtterance();
speech.rate = 1;
speech.pitch = 1;
speech.volume = 1;
speech.voice = speechSynthesis.getVoices()[0];

export default {
  name: "TextVoiceApp",

  methods: {
    speakInputText() {
      // Esta funcion convierte en audio el texto escrito.
      let text = document.getElementById("textArea").value;
      if (text != "") {
        //Este condicional determina, si no hay nada escrito te pide ingresar algo, en el caso contrario se reproduce lo escrito.
        speech.text = document.getElementById("textArea").value;
        speechSynthesis.speak(speech);
      } else {
        text = "No has ingresado nada, por favor escribe algo";
        speech.text = text;
        speechSynthesis.speak(speech);
      }
    },
    stopText() {
      speechSynthesis.cancel();
    },
  },
};
</script>

<style scoped>
.container-all {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 750px;
  background-image: url("./assets/back3.jpg");
}

.container-logo {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
  margin-bottom: 50px;
}

img {
  width: 300px;
}

.btn {
  width: 120px;
  height: 35px;
  font-size: 16px;
  border-radius: 20px;
  border-color: rgba(255, 255, 255, 0.1);
  outline-color: rgba(255, 255, 255, 0.1);
  margin-top: 40px;
  font-family: monospace;
}

.container-all textarea {
  width: 42%;
  height: 50%;
  min-width: 42%;
  max-width: 42%;
  min-height: 50%;
  max-height: 50%;
  padding-left: 12px;
  padding-top: 12px;
  margin-top: 12px;
  border-radius: 20px;
  font-size: 22px;
  background: rgba(255, 255, 255, 0.2);
  outline-color: rgba(255, 255, 255, 0.1);
  border-color: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(7px);
}

textarea::placeholder {
  color: white;
}

.container-btn {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-play {
  width: 400px;
  background: rgba(58, 235, 4, 0.2);
  outline-color: rgba(24, 245, 3, 0.1);
  border-color: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(7px);
  transition-duration: 0.2s;
}

.btn-stop {
  width: 120px;
  margin-left: 10px;
  background: rgba(241, 3, 3, 0.2);
  outline-color: rgba(255, 255, 255, 0.1);
  border-color: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(7px);
  transition-duration: 0.2s;
}

.container-btn .btn-play,
.btn-stop {
  height: 50px;
  border-radius: 20px;
  font-size: 20px;
  color: white;
  margin-top: 10px;
  border: none;
}

.btn-play:hover {
  background-color: #006400;
  width: 425px;
  height: 52px;
}

.btn-stop:hover {
  background-color: #8b0000;
  width: 123px;
  height: 52px;
}

i {
  margin-left: 10px;
}
</style>