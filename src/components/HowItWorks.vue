<template>
  <section id="como-funciona" class="how-it-works">
    <div class="container">
      <h2 class="section-title">¿Cómo Funciona?</h2>
      <div class="title-underline"></div>
      <p class="section-subtitle">
        El proceso de intermediación es simple, seguro y transparente
      </p>

      <div class="steps-grid">
        <div class="step-card" v-for="(step, index) in steps" :key="index">
          <div class="step-number">{{ index + 1 }}</div>
          <div class="step-icon" aria-hidden="true">
            <!-- Outline Chat Bubble -->
            <svg v-if="index === 0" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <path d="M21 12a7 7 0 0 1-7 7H9l-4 3v-3a7 7 0 0 1-2-5 7 7 0 0 1 7-7h4a7 7 0 0 1 7 7Z" fill="none"/>
            </svg>
            <!-- Outline Magnifying Glass -->
            <svg v-else-if="index === 1" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <circle cx="11" cy="11" r="6" fill="none"/>
              <path d="M20 20l-3.5-3.5" fill="none"/>
            </svg>
            <!-- Outline Shield with Check -->
            <svg v-else-if="index === 2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <path d="M12 3l7 3v6c0 5-3.5 9-7 9s-7-4-7-9V6l7-3Z" fill="none"/>
              <path d="M8.5 12.5l2.5 2.5 4.5-4.5" fill="none"/>
            </svg>
            <!-- Outline Badge/Check -->
            <svg v-else viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <circle cx="12" cy="12" r="8" fill="none"/>
              <path d="M9 12l2 2 4-4" fill="none"/>
            </svg>
          </div>
          <h3 class="step-title">{{ step.title }}</h3>
          <p class="step-description">{{ step.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const steps = [
  {
    icon: '📞',
    title: 'Contacto Inicial',
    description: 'El vendedor y comprador me contactan. Verifico la información de ambas partes y coordino los detalles de la transacción.'
  },
  {
    icon: '🔍',
    title: 'Verificación',
    description: 'Reviso la cuenta de Free Fire, confirmo los datos, estadísticas y que todo esté en orden antes de proceder.'
  },
  {
    icon: '💰',
    title: 'Transacción Segura',
    description: 'Coordino el pago y la transferencia de la cuenta. El dinero se maneja de forma transparente y segura.'
  },
  {
    icon: '✅',
    title: 'Entrega Final',
    description: 'Una vez confirmado el pago, se realiza la transferencia de la cuenta al comprador. Ambas partes quedan satisfechas.'
  }
]
</script>

<style scoped>
.how-it-works {
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

.steps-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2.5rem;
}

.step-card {
  background: linear-gradient(135deg, var(--color-gray) 0%, var(--color-light-gray) 100%);
  padding: 2.5rem 2rem;
  border-radius: 15px;
  text-align: center;
  position: relative;
  transition: all 0.3s ease;
  border: 2px solid transparent;
}

.step-card:hover {
  transform: translateY(-10px);
  border-color: var(--color-gold);
  box-shadow: 0 15px 40px rgba(212, 175, 55, 0.2);
}

.step-number {
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
  width: 45px;
  height: 45px;
  background: linear-gradient(135deg, var(--color-gold) 0%, #f4d03f 100%);
  color: var(--color-black);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.3rem;
  font-weight: 700;
  box-shadow: 0 5px 15px rgba(212, 175, 55, 0.4);
}

.step-icon {
  margin: 1rem auto;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 4rem;
  height: 4rem;
}

.step-icon svg {
  width: 100%;
  height: 100%;
  fill: none;
  stroke: var(--color-gold);
  stroke-width: 2;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.step-title {
  font-size: 1.5rem;
  color: var(--color-gold);
  margin-bottom: 1rem;
  font-weight: 700;
}

.step-description {
  font-size: 1rem;
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.6;
}

@media (max-width: 768px) {
  .how-it-works {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2rem;
  }

  .steps-grid {
    gap: 3rem;
  }
}
</style>
