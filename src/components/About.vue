<template>
  <section id="sobre-mi" class="about">
    <div class="container">
      <div class="about-content">
        <div class="about-image">
          <div class="image-placeholder">
            <img src="../assets/perfil.jpg" alt="Foto de perfil" />
          </div>
        </div>
        <div class="about-text">
          <h2 class="section-title">Sobre Mí</h2>
          <div class="title-underline"></div>
          <h3 class="about-name">Tu Intermediario de Confianza</h3>
          <p class="about-description">
            Soy un administrador profesional especializado en facilitar cambios y ventas de cuentas de Free Fire.
            Mi trabajo es actuar como intermediario entre compradores y vendedores, garantizando transacciones
            seguras, transparentes y legales.
          </p>
          <p class="about-description">
            Con años de experiencia en el mercado, he ayudado a cientos de jugadores a realizar sus transacciones
            de forma confiable. Mi compromiso es ofrecer un servicio profesional donde la <strong>seguridad</strong>
            y la <strong>transparencia</strong> son la prioridad.
          </p>
          <div class="about-features">
            <div class="feature-item">
              <span class="feature-icon">✅</span>
              <span>100% Transparente</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">🔒</span>
              <span>Transacciones Seguras</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">⚡</span>
              <span>Proceso Rápido</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 6rem 0;
  background-color: var(--color-gray);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 4rem;
  align-items: center;
}

.about-image {
  display: flex;
  justify-content: center;
}

.image-placeholder {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, var(--color-light-gray) 0%, var(--color-gray) 100%);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 3px solid var(--color-gold);
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
}

.image-placeholder img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
  display: block;
}

.icon {
  font-size: 8rem;
  opacity: 0.5;
}

.section-title {
  font-size: 2.5rem;
  color: var(--color-white);
  margin-bottom: 1rem;
}

.title-underline {
  width: 80px;
  height: 4px;
  background: linear-gradient(90deg, var(--color-gold) 0%, transparent 100%);
  margin-bottom: 1.5rem;
}

.about-name {
  font-size: 1.8rem;
  color: var(--color-gold);
  margin-bottom: 1.5rem;
}

.about-description {
  font-size: 1.1rem;
  color: rgba(255, 255, 255, 0.85);
  margin-bottom: 1.5rem;
  line-height: 1.8;
}

.about-features {
  display: flex;
  gap: 2rem;
  margin-top: 2rem;
  flex-wrap: wrap;
}

.feature-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 1rem;
  color: var(--color-white);
  font-weight: 600;
}

.feature-icon {
  font-size: 1.5rem;
}

@media (max-width: 968px) {
  .about-content {
    grid-template-columns: 1fr;
    gap: 3rem;
  }

  .image-placeholder {
    width: 250px;
    height: 250px;
  }

  .icon {
    font-size: 6rem;
  }
}

@media (max-width: 768px) {
  .about {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2rem;
  }

  .about-name {
    font-size: 1.5rem;
  }

  .about-features {
    flex-direction: column;
    gap: 1rem;
  }
}
</style>
