<template>
  <div>
    <nav class="navbar">
      <div class="logo">
        <img src="~/assets/img/logo.png" alt="Logo Sekolah" />
        <div class="school-info">
          <h1>SMKN 4 TASIKMALAYA</h1>
          <p>Jl. Depok, Sukamenak, Kec. Purbaratu, Kab. Tasikmalaya, Jawa Barat 46196</p>
        </div>
      </div>
      <ul class="nav-links" :class="{ active: isMenuActive }">
        <li><NuxtLink to="/">BERANDA</NuxtLink></li>
        <li><NuxtLink to="/profil">PROFIL</NuxtLink></li>
        <li><NuxtLink to="/jurusan">PROGRAM KEAHLIAN</NuxtLink></li>
        <li><NuxtLink to="/ekskul">EKSTRAKURIKULER</NuxtLink></li>
        <li><NuxtLink to="/galeri">GALERI</NuxtLink></li>
      </ul>
      <div class="menu-toggle" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuActive: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuActive = !this.isMenuActive;
    },
  },
};
</script>

<style scoped>
/* General Navbar Styles */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #4998f9;
  color: #ffffff;
  padding: 1rem 2rem;
  flex-wrap: wrap;
}

.logo {
  display: flex;
  align-items: center;
}

.logo img {
  width: 50px;
  height: auto;
  margin-right: 10px;
}

.school-info h1 {
  font-size: 1.2em;
  margin: 0;
}

.school-info p {
  font-size: 0.8em;
  margin: 0;
}

/* Navigation Links */
.nav-links {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}

.nav-links li {
  margin-left: 20px;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #ccc;
}

/* Responsive Navbar */
.menu-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.menu-toggle span {
  background: #fff;
  height: 3px;
  width: 25px;
  margin: 4px 0;
  transition: all 0.3s ease;
}

@media (max-width: 768px) {
  .menu-toggle {
    display: flex;
  }

  .nav-links {
    display: none;
    flex-direction: column;
    background-color: #44abf0;
    position: absolute;
    top: 70px;
    right: 0;
    width: 100%;
    text-align: center;
    z-index: 1000;
  }

  .nav-links.active {
    display: flex;
  }

  .nav-links li {
    margin: 10px 0;
  }
}
</style>
