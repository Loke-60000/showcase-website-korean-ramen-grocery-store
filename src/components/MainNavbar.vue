<template>
  <header>
    <div class="navbar">
      <div class="logo">
        <RouterLink to="/"><img class="logo" :src="logo" alt="" srcset=""></RouterLink>
      </div>
      <ul class="links">
        <li>
          <RouterLink to="/">Home</RouterLink>
        </li>
        <li>
          <RouterLink to="/about">A propos</RouterLink>
        </li>
        <li>
          <RouterLink to="/gallery">Gallerie</RouterLink>
        </li>
      </ul>
      <RouterLink to="/contact" class="action_btn">Contactez nous</RouterLink>
      <button class="toggle_btn" @click="toggleDropdown">
        <img src="https://www.clipartmax.com/png/small/36-365828_navbar-toggle-icon-menu-hamburger-png-white.png" alt="Menu" />
      </button>
    </div>
    <ul class="dropdown_menu" :class="{ open: isOpen }">
      <li><RouterLink to="/">Home</RouterLink></li>
      <li><RouterLink to="/about">About</RouterLink></li>
      <li><RouterLink to="/gallery">Gallery</RouterLink></li>
      <li>
        <RouterLink to="/contact">Contactez nous</RouterLink>
      </li>
    </ul>
  </header>
</template>

<script>
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
import logo from "../assets/logo.png";

export default {
  name: "MainNavbar",
  setup() {
    const isOpen = ref(false);

    function toggleDropdown() {
      isOpen.value = !isOpen.value;
    }

    return {
      isOpen,
      toggleDropdown,
      logo,
    };
  },
};
</script>
<style scoped>
:root {
  --main-color: #ffc40e;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

.logo {
  height: 100px;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
  color: white;
}

/* a:hover {
  color: orange;
} */

header {
  position: fixed;
  padding: 0 2rem;
  background-color: var(--main-color);
  width: 100%;
  z-index: 1000;
  left: 0;
}

.navbar {
  display: flex;
  width: 100%;
  height: 100px;
  max-width: 1200px;
  margin: 0 auto;
  align-items: center;
  justify-content: space-between;
}

.navbar .links {
  display: flex;
  gap: 2rem;
}

.toggle_btn {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
}

.toggle_btn img {
  width: 24px;
  height: 24px;
}

.action_btn,
.dropdown_menu li {
  background-color: orange;
  color: white;
  font-weight: bold;
}

.action_btn {
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 1rem;
  transition: transform 0.2s;
}

.action_btn:hover {
  transform: scale(1.05);
}

.action_btn:active {
  transform: scale(0.95);
}

.dropdown_menu {
  display: none;
  position: absolute;
  background-color: var(--main-color);
  backdrop-filter: blur(15px);
  top: 100px;
  left: 0;
  height: 0;
  width: 100%;
  overflow: hidden;
  transition: 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.dropdown_menu li {
  padding: 0.7rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.dropdown_menu.open {
  height: 190px;
}

@media (max-width: 992px) {
  .navbar .links,
  .navbar .action_btn {
    display: none;
  }
  .toggle_btn {
    display: block;
  }
  .dropdown_menu {
    display: block;
  }
}

@media (max-width: 576px) {
  .dropdown_menu {
    width: 100%;
  }
}

@media (max-width: 500px) {
  .logo {
    height: 50px;
  }
}
</style>
