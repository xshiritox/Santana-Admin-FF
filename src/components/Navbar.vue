<script setup lang="ts">
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
  mobileMenuOpen.value = false
}
</script>

<template>
  <nav class="navbar">
    <div class="container">
      <div class="nav-brand">
        <span class="brand-icon">🔥</span>
        <span class="brand-text">Santana Admin-FF</span>
      </div>

      <button class="mobile-toggle" @click="toggleMobileMenu" :class="{ active: mobileMenuOpen }">
        <span></span>
        <span></span>
        <span></span>
      </button>

      <ul class="nav-menu" :class="{ active: mobileMenuOpen }">
        <li><a @click="scrollToSection('inicio')">Inicio</a></li>
        <li><a @click="scrollToSection('sobre-mi')">Sobre Mí</a></li>
        <li><a @click="scrollToSection('como-funciona')">Cómo Funciona</a></li>
        <li><a @click="scrollToSection('testimonios')">Testimonios</a></li>
        <li><a @click="scrollToSection('contacto')">Contacto</a></li>
        <li><a @click="scrollToSection('politicas')">Políticas</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background-color: rgba(10, 10, 10, 0.95);
  backdrop-filter: blur(10px);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 1rem 0;
  box-shadow: 0 2px 10px rgba(212, 175, 55, 0.1);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-brand {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-gold);
}

.brand-icon {
  font-size: 1.8rem;
}

.brand-text {
  color: var(--color-white);
}

.mobile-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  padding: 0.5rem;
}

.mobile-toggle span {
  display: block;
  width: 25px;
  height: 3px;
  background-color: var(--color-gold);
  transition: all 0.3s ease;
}

.mobile-toggle.active span:nth-child(1) {
  transform: rotate(45deg) translate(8px, 8px);
}

.mobile-toggle.active span:nth-child(2) {
  opacity: 0;
}

.mobile-toggle.active span:nth-child(3) {
  transform: rotate(-45deg) translate(7px, -7px);
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 2rem;
  align-items: center;
}

.nav-menu li a {
  color: var(--color-white);
  font-weight: 500;
  cursor: pointer;
  transition: color 0.3s ease;
  position: relative;
}

.nav-menu li a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--color-gold);
  transition: width 0.3s ease;
}

.nav-menu li a:hover {
  color: var(--color-gold);
}

.nav-menu li a:hover::after {
  width: 100%;
}

@media (max-width: 768px) {
  .mobile-toggle {
    display: flex;
  }

  .nav-menu {
    position: fixed;
    top: 70px;
    left: -100%;
    flex-direction: column;
    background-color: rgba(10, 10, 10, 0.98);
    width: 100%;
    padding: 2rem;
    gap: 1.5rem;
    transition: left 0.3s ease;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
  }

  .nav-menu.active {
    left: 0;
  }

  .nav-menu li a {
    font-size: 1.2rem;
  }
}
</style>
