<script setup lang="ts">
const openWhatsApp = () => {
  window.open('https://wa.me/1234567890', '_blank')
}
</script>

<template>
  <section id="inicio" class="hero">
    <div class="hero-overlay"></div>
    <div class="hero-content">
      <h1 class="hero-title">
        Administrador de Cambios y Ventas
        <span class="highlight">de Cuentas de Free Fire</span>
      </h1>
      <p class="hero-subtitle">
        Garantizo transacciones seguras y legales. Tu confianza es mi prioridad.
      </p>
      <button class="cta-button" @click="openWhatsApp">
        <span class="whatsapp-icon">📱</span>
        Contactar por WhatsApp
      </button>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url('../assets/FF.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(10, 10, 10, 0.9) 0%, rgba(42, 42, 42, 0.85) 100%);
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
  padding: 2rem;
  text-align: center;
  animation: fadeInUp 1s ease-out;
}

.hero-title {
  font-size: 3rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  color: var(--color-white);
  line-height: 1.2;
}

.highlight {
  display: block;
  color: var(--color-gold);
  margin-top: 0.5rem;
}

.hero-subtitle {
  font-size: 1.3rem;
  color: var(--color-white);
  margin-bottom: 2.5rem;
  opacity: 0.9;
}

.cta-button {
  background: linear-gradient(135deg, var(--color-gold) 0%, #f4d03f 100%);
  color: var(--color-black);
  border: none;
  padding: 1rem 2.5rem;
  font-size: 1.1rem;
  font-weight: 700;
  border-radius: 50px;
  display: inline-flex;
  align-items: center;
  gap: 0.8rem;
  transition: all 0.3s ease;
  box-shadow: 0 5px 20px rgba(212, 175, 55, 0.4);
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 30px rgba(212, 175, 55, 0.6);
}

.whatsapp-icon {
  font-size: 1.5rem;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2rem;
  }

  .hero-subtitle {
    font-size: 1.1rem;
  }

  .cta-button {
    padding: 0.9rem 2rem;
    font-size: 1rem;
  }
}
</style>
