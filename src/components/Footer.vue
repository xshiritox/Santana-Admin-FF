<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-brand">
          <h3 class="brand-name">
            <span class="brand-icon">🔥</span>
            FF Admin
          </h3>
          <p class="brand-tagline">
            Tu intermediario de confianza para transacciones seguras de cuentas de Free Fire
          </p>
        </div>

        <div class="footer-links">
          <h4>Enlaces Rápidos</h4>
          <ul>
            <li><a @click="scrollToSection('inicio')">Inicio</a></li>
            <li><a @click="scrollToSection('sobre-mi')">Sobre Mí</a></li>
            <li><a @click="scrollToSection('como-funciona')">Cómo Funciona</a></li>
            <li><a @click="scrollToSection('contacto')">Contacto</a></li>
          </ul>
        </div>

        <div class="footer-contact">
          <h4>Contacto</h4>
          <div class="contact-item">
            <span class="contact-icon">📱</span>
            <span>WhatsApp</span>
          </div>
          <div class="contact-item">
            <span class="contact-icon">📷</span>
            <span>Instagram</span>
          </div>
          <div class="contact-item">
            <span class="contact-icon">📘</span>
            <span>Facebook</span>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <p>&copy; 2025 FF Admin. Todos los derechos reservados.</p>
        <p class="footer-disclaimer">
          Servicio de intermediación profesional. No afiliado con Garena o Free Fire.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<style scoped>
.footer {
  background-color: var(--color-black);
  padding: 3rem 0 1.5rem;
  border-top: 2px solid var(--color-gold);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.footer-content {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 3rem;
  margin-bottom: 2rem;
}

.footer-brand {
  max-width: 350px;
}

.brand-name {
  font-size: 1.8rem;
  color: var(--color-white);
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.brand-icon {
  font-size: 2rem;
}

.brand-tagline {
  color: rgba(255, 255, 255, 0.7);
  line-height: 1.6;
}

.footer-links h4,
.footer-contact h4 {
  color: var(--color-gold);
  font-size: 1.2rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.footer-links ul {
  list-style: none;
}

.footer-links li {
  margin-bottom: 0.8rem;
}

.footer-links a {
  color: rgba(255, 255, 255, 0.7);
  cursor: pointer;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--color-gold);
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 0.8rem;
}

.contact-icon {
  font-size: 1.3rem;
}

.footer-bottom {
  border-top: 1px solid var(--color-light-gray);
  padding-top: 1.5rem;
  text-align: center;
}

.footer-bottom p {
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.9rem;
  margin-bottom: 0.5rem;
}

.footer-disclaimer {
  font-size: 0.8rem;
  font-style: italic;
}

@media (max-width: 968px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .footer-brand {
    max-width: 100%;
  }
}

@media (max-width: 768px) {
  .footer {
    padding: 2rem 0 1rem;
  }

  .brand-name {
    font-size: 1.5rem;
  }
}
</style>
