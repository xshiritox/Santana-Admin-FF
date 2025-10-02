<template>
  <section id="testimonios" class="testimonials">
    <div class="container">
      <h2 class="section-title">Lo Que Dicen Mis Clientes</h2>
      <div class="title-underline"></div>
      <p class="section-subtitle">
        Testimonios reales de personas que confiaron en mi servicio
      </p>

      <div class="testimonials-grid">
        <div class="testimonial-card" v-for="(testimonial, index) in testimonials" :key="index">
          <div class="stars">
            <span v-for="star in 5" :key="star" class="star">⭐</span>
          </div>
          <p class="testimonial-text">"{{ testimonial.text }}"</p>
          <div class="testimonial-author">
            <div class="author-avatar" aria-hidden="true">
              <!-- Outline Person Icon -->
              <svg v-if="testimonial.avatar === 'person'" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
                <circle cx="12" cy="8" r="3" fill="none"/>
                <path d="M12 12c-4 0-6 2-6 4v1h12v-1c0-2-2-4-6-4Z" fill="none"/>
              </svg>
            </div>
            <div class="author-info">
              <h4 class="author-name">{{ testimonial.name }}</h4>
              <p class="author-role">{{ testimonial.role }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const testimonials = [
  {
    text: 'Nada de estafas todo legal bro gracias',
    name: 'Carlos',
    role: 'Comprador',
    avatar: 'person'
  },
  {
    text: 'Trato super rapido y confiable gente se los recomiendo',
    name: 'José Pérez',
    role: 'Vendedor',
    avatar: 'person'
  },
  {
    text: '100% recomendado mi gente.',
    name: 'Luis Rodriguez',
    role: 'Comprador',
    avatar: 'person'
  },
  {
    text: 'Gracias mi rey todo totalmente legal, recomendado 100/100',
    name: 'Bismar',
    role: 'Comprador',
    avatar: 'person'
  },
  {
    text: 'Todo confiable bro gracias',
    name: 'Miguel Angel',
    role: 'Comprador',
    avatar: 'person'
  },
  {
    text: 'Se los recomiendo confiable y rapido',
    name: 'Sandra',
    role: 'Vendedora',
    avatar: 'person'
  }
]
</script>

<style scoped>
.testimonials {
  padding: 6rem 0;
  background-color: var(--color-gray);
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

.author-avatar {
  display: inline-flex;
  width: 4rem;
  height: 4rem;
  align-items: center;
  justify-content: center;
}

.author-avatar svg {
  width: 100%;
  height: 100%;
  fill: none;
  stroke: var(--color-gold);
  stroke-width: 3;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.testimonial-card {
  background: linear-gradient(135deg, var(--color-light-gray) 0%, var(--color-gray) 100%);
  padding: 2rem;
  border-radius: 15px;
  border: 2px solid transparent;
  transition: all 0.3s ease;
}

.testimonial-card:hover {
  transform: translateY(-5px);
  border-color: var(--color-gold);
  box-shadow: 0 10px 30px rgba(212, 175, 55, 0.2);
}

.stars {
  display: flex;
  gap: 0.3rem;
  margin-bottom: 1rem;
}

.star {
  font-size: 1.2rem;
}

.testimonial-text {
  font-size: 1rem;
  color: rgba(255, 255, 255, 0.9);
  line-height: 1.6;
  margin-bottom: 1.5rem;
  font-style: italic;
}

.testimonial-author {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.author-avatar {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--color-gold) 0%, #f4d03f 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
}

.author-name {
  font-size: 1.1rem;
  color: var(--color-gold);
  font-weight: 700;
  margin-bottom: 0.2rem;
}

.author-role {
  font-size: 0.9rem;
  color: rgba(255, 255, 255, 0.6);
}

@media (max-width: 768px) {
  .testimonials {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2rem;
  }

  .testimonials-grid {
    gap: 1.5rem;
  }
}
</style>
