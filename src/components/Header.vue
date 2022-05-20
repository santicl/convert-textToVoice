<template>
  <header>
    <nav>
      <div class="container-nav">
        <img src="./assets/S.png" alt="" />
        <ul>
          <li><a href="#">Inicio</a></li>
          <li><a href="#">Servicios</a></li>
          <li class="nav-mini">
            <a href="https://santydev.netlify.app/">SantyDev</a>
            <ul class="ul">
                <li><button>Vistar sitio web</button></li>
            </ul>
          </li>
          <li><a href="#">Contacto</a></li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
  background-color: black;
  color: white;
}

.container-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 20px;
}

.container-nav ul {
  display: flex;
  justify-content: space-between;
  list-style: none;
}

.container-nav ul a {
  text-decoration: none;
}

li {
  font-size: 20px;
  margin: 30px;
  transition-duration: 0.2s;
}

div ul {
  display: flex;
  justify-content: center;
  align-items: center;
}
div ul li {
  list-style: none;
  margin-left: 20px;
}

img {
    width: 250px;
}

div ul li a {
  text-decoration: none;
  padding: 6px 15px;
  color: #fff;
  border-radius: 20px;
}

div ul li a:hover {
  background: #fff;
  color: black;
}

h1 {
  margin: 10px;
}

li ul{
  display: none;
  visibility: hidden;
  position: absolute;
  background: #fff;
  box-shadow: 0px 0px 30px rgba(127, 137, 161, 0.25);
  transition: 0.3s;
}

.nav-mini:hover > ul{
  display: block;
  visibility: visible;
  opacity: 1;
  top: 0;
  left: 100%;
}

.ul {
    background: rgba(0, 0, 0, 0.8);
}

</style>