<script setup></script>
<template>
  <header>
    <img src="../assets/img/logo (1).svg" alt="" />

    <nav>
      <a href="http://">SCIENCES ⏷</a>
      <a href="http://">SANTE ⏷</a>
      <a href="http://">TECH ⏷</a>
      <a href="http://">MAISON ⏷</a>
      <a href="http://">PLANETE ⏷</a>
    </nav>

    <button>JE M'ABONNE</button>
  </header>
</template>

<style scoped>
header {
  height: 60px;
  background: linear-gradient(45deg, #be80ff, #6325ff);
  padding: 10px 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav {
  display: flex;
  gap: 25px;
  color: white;
}

a {
  text-decoration: none;
  color: white;
  display: flex;
  gap: 5px;
}

h1 {
  font-size: 30px;
  color: white;
}

button {
  background-color: #fdb00f;
  border: none;
  color: white;
  padding: 7px 15px;
}
</style>
