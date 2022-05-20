<template>
  <section class="section">
    <div class="container-section">
      <section class="container-about">
        <div class="about_btnURL">
          <h2>
          About<button class="btn">
            <strong>TextVoice</strong
            ><i class="fa fa-microphone" aria-hidden="true"></i>
          </button>
        </h2>
        <p>Esta extensión permitirá leer cualquier sitio web.</p>
        <p>
          Esta extensión fue creada para las personas que necesitan un descanso
          visual y que, a la vez, no pierda el tiempo esperando a que se haya
          pasado el malestar en los ojos.
        </p>
        <div class="container-URL_PAGE_DEV">
          <h3>Ir a página del desarrollador</h3>
          <button class="btn_URL-DEV"><a href="https://santydev.netlify.app/">Ir a SantyDev</a></button>
        </div>
        </div>
      </section>
      <div class="container-img">
        <img src="./assets/about.png" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionAboutProyect",
};
</script>

<style scope>
* {
  margin: 0;
  padding: 0;
}

.section {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url("./assets/back3.jpg");
}

.container-section {
  display: flex;
  justify-content: space-between;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
  width: 97%;
  height: 75vh;
  background: rgba(255, 255, 255, 0.2);
  outline-color: rgba(255, 255, 255, 0.1);
  border-color: rgba(255, 255, 255, 0.1);
  border-radius: 30px;
  backdrop-filter: blur(12px);
}

.container-about {
  display: flex;
  flex-direction: column;
  width: 40%;
  margin-right: 100px;
}

.about_btnURL {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.container-about h2 {
  margin-bottom: 50px;
  font-size: 50px;
}

.container-about .btn {
  width: 250px;
  height: 60px;
  font-size: 25px;
  border-radius: 45px;
  margin-left: 12px;
  border-color: rgba(255, 255, 255, 0.1);
  outline-color: rgba(255, 255, 255, 0.1);
  font-family: monospace;
}

.container-about .btn i {
  margin-left: 10px;
}

img {
  width: 450px;
}

p {
  font-size: 25px;
}

h2,
p,
h3 {
  color: white;
}

.container-URL_PAGE_DEV {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 400px;
  height: 55px;
  padding-right: 10px;
  padding-left: 10px;
  margin-top: 50px;
  background: rgba(255, 255, 255, 0.2);
  outline-color: rgba(255, 255, 255, 0.1);
  border-color: rgba(255, 255, 255, 0.1);
  border-radius: 30px;
  backdrop-filter: blur(12px);
}

.btn_URL-DEV {
  width: 120px;
  height: 30px;
  background: rgba(59, 131, 4189, .4);
  font-size: 10px;
  outline-color: rgba(59, 131, 4189, 0.1);
  border-color: rgba(59, 131, 4189, 0.1);
  border-radius: 15px;
  backdrop-filter: blur(5px);
  transition-duration: 0.2s;
}

.btn_URL-DEV a {
    text-decoration: none;
    color: white;
}

.btn_URL-DEV:hover {
  background-color: rgba(59, 131, 4189, .9);
  outline-color: rgba(59, 131, 4189, 0.1);
  border-color: rgba(59, 131, 4189, 0.1);
  width: 130px;
  height: 40px;
}
</style>
