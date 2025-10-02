<script setup lang="ts">
const openWhatsApp = () => {
  window.open('https://wa.me/5353547990?text=*SOLICITUD%20DE%20INTERMEDIARIO.*%0A%0AHola%20buenas%2C%20estoy%20interesado%20en%20contratar%20tus%20servicios%20de%20administraci%C3%B3n%20de%20cambios%2C%20compras%20y%20ventas%20de%20cuentas%20de%20Free%20Fire.', '_blank')
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
        <span class="whatsapp-icon" aria-hidden="true">
          <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
            <path d="M19.11 17.39c-.28-.14-1.65-.81-1.9-.9-.26-.1-.45-.14-.64.14-.19.28-.73.9-.89 1.08-.16.19-.33.21-.61.07-.28-.14-1.16-.43-2.2-1.37-.81-.72-1.36-1.61-1.52-1.89-.16-.28-.02-.43.12-.57.13-.13.28-.33.42-.49.14-.16.19-.28.28-.47.09-.19.05-.36-.02-.5-.07-.14-.64-1.54-.88-2.11-.23-.56-.47-.49-.64-.5-.16-.01-.35-.01-.54-.01s-.5.07-.76.36c-.26.28-1.01.99-1.01 2.42 0 1.43 1.03 2.81 1.18 3 .14.19 2.03 3.1 4.92 4.35.69.3 1.23.48 1.65.61.69.22 1.32.19 1.82.12.56-.08 1.65-.67 1.88-1.32.23-.65.23-1.21.16-1.33-.07-.12-.26-.19-.54-.33zM16 3C8.83 3 3 8.83 3 16c0 2.3.62 4.46 1.69 6.32L3 29l6.86-1.8C11.63 28.38 13.74 29 16 29c7.17 0 13-5.83 13-13S23.17 3 16 3zm0 23.64c-2.13 0-4.1-.62-5.76-1.68l-.41-.26-4.08 1.08 1.09-3.98-.27-.41A10.61 10.61 0 0 1 5.36 16c0-5.87 4.77-10.64 10.64-10.64S26.64 10.13 26.64 16 21.87 26.64 16 26.64z"/>
          </svg>
        </span>
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
  display: inline-flex;
  width: 1.5rem;
  height: 1.5rem;
}

.whatsapp-icon svg {
  width: 100%;
  height: 100%;
  fill: #25D366; /* WhatsApp green */
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
