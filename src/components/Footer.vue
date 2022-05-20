<template>
  <footer class="container-footer">
    <div class="copyright-box">
      <p class="copyright">
        &copy; Copyright <strong>Santiago C Suarez</strong>. Todos los derechos
        reservados
      </p>
      <div class="credits">
        Diseñado por <a href="https://github.com/santicl">Santiago C Suarez</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  background-color: black;
  color: white;
}

footer {
    height: 100px;
}

.container-footer {
  display: flex;
  justify-content: center;
  align-items: center;
}

.copyright-box, .credits{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.copyright {
    font-size: 16px;
}

.credits {
    font-size: 16px;
}

.credits a {
    text-decoration: none;
}
</style>
