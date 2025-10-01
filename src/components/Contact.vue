<script setup lang="ts">
const openSocial = (platform: string) => {
  const urls: Record<string, string> = {
    whatsapp: 'https://wa.me/1234567890',
    instagram: 'https://instagram.com/tu_usuario',
    facebook: 'https://facebook.com/tu_pagina'
  }
  window.open(urls[platform], '_blank')
}
</script>

<template>
  <section id="contacto" class="contact">
    <div class="container">
      <h2 class="section-title">Contacto</h2>
      <div class="title-underline"></div>
      <p class="section-subtitle">
        ¿Listo para hacer tu transacción? Contáctame por cualquiera de estos medios
      </p>

      <div class="social-buttons">
        <button class="social-btn whatsapp" @click="openSocial('whatsapp')">
          <span class="social-icon">📱</span>
          <span>WhatsApp</span>
        </button>
        <button class="social-btn instagram" @click="openSocial('instagram')">
          <span class="social-icon">📷</span>
          <span>Instagram</span>
        </button>
        <button class="social-btn facebook" @click="openSocial('facebook')">
          <span class="social-icon">📘</span>
          <span>Facebook</span>
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  padding: 6rem 0;
  background-color: var(--color-black);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-title {
  font-size: 2.5rem;
  color: var(--color-white);
  text-align: center;
  margin-bottom: 1rem;
}

.title-underline {
  width: 80px;
  height: 4px;
  background: var(--color-gold);
  margin: 0 auto 1.5rem;
}

.section-subtitle {
  text-align: center;
  font-size: 1.2rem;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 4rem;
}

.social-buttons {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  max-width: 500px;
  margin: 0 auto;
}

.social-btn {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.2rem 2rem;
  border: none;
  border-radius: 10px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  color: var(--color-white);
}

.social-btn.whatsapp {
  background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
}

.social-btn.instagram {
  background: linear-gradient(135deg, #E1306C 0%, #C13584 100%);
}

.social-btn.facebook {
  background: linear-gradient(135deg, #1877F2 0%, #0C63D4 100%);
}

.social-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
}

.social-icon {
  font-size: 1.5rem;
}

@media (max-width: 768px) {
  .contact {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2rem;
  }

  .social-buttons {
    max-width: 100%;
  }
}
</style>
