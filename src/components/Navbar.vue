<template>
  <nav class="navbar">
    <div class="logo">Showroom Motor Custome</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center; /* Rata tengah secara vertikal */
  background-color: #0a1519;
  padding: 10px;
}

.logo {
  color: #ffffff;
  font-size: 24px;
  font-family: 'Broadway'
  
}
.nav-links {
  list-style: none;
  display: flex;
}
.nav-links li {
  margin: 0 10px;
}
.nav-links a {
  color: #000000;
  text-decoration: none;
}


</style>
