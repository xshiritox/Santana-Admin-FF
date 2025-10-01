<template>
  <section id="politicas" class="policies">
    <div class="container">
      <h2 class="section-title">Políticas y Términos</h2>
      <div class="title-underline"></div>

      <div class="policies-content">
        <div class="policy-card">
          <div class="policy-icon">📋</div>
          <h3 class="policy-title">Rol de Intermediario</h3>
          <p class="policy-text">
            <strong>Importante:</strong> No vendo cuentas directamente. Mi función es actuar como
            <strong>intermediario profesional</strong> entre compradores y vendedores, garantizando
            que las transacciones se realicen de forma segura y transparente.
          </p>
        </div>

        <div class="policy-card">
          <div class="policy-icon">⚖️</div>
          <h3 class="policy-title">Aviso Legal</h3>
          <p class="policy-text">
            No me hago responsable de cuentas que incumplan las normas de Garena o Free Fire.
            Es responsabilidad del vendedor asegurar que la cuenta esté libre de sanciones,
            restricciones o violaciones de términos de servicio.
          </p>
        </div>

        <div class="policy-card">
          <div class="policy-icon">🔒</div>
          <h3 class="policy-title">Seguridad y Transparencia</h3>
          <p class="policy-text">
            Todas las transacciones son verificadas antes de proceder. Solicito información
            completa de la cuenta y coordino directamente con ambas partes para asegurar que
            todo esté en orden antes de finalizar cualquier operación.
          </p>
        </div>

        <div class="policy-card">
          <div class="policy-icon">💼</div>
          <h3 class="policy-title">Compromiso Profesional</h3>
          <p class="policy-text">
            Me comprometo a mantener la confidencialidad de la información compartida, actuar
            con honestidad en cada transacción, y brindar soporte durante todo el proceso para
            garantizar la satisfacción de ambas partes.
          </p>
        </div>
      </div>

      <div class="disclaimer">
        <p>
          <strong>Nota:</strong> Al utilizar mis servicios, aceptas que he actuado únicamente como
          intermediario en la transacción. Es tu responsabilidad verificar que las cuentas cumplan
          con los términos de servicio de Free Fire y Garena.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.policies {
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
  margin: 0 auto 3rem;
}

.policies-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.policy-card {
  background: var(--color-light-gray);
  padding: 2rem;
  border-radius: 15px;
  border: 2px solid transparent;
  transition: all 0.3s ease;
}

.policy-card:hover {
  border-color: var(--color-gold);
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(212, 175, 55, 0.15);
}

.policy-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.policy-title {
  font-size: 1.5rem;
  color: var(--color-gold);
  margin-bottom: 1rem;
  font-weight: 700;
}

.policy-text {
  font-size: 1rem;
  color: rgba(255, 255, 255, 0.85);
  line-height: 1.7;
}

.policy-text strong {
  color: var(--color-gold);
  font-weight: 600;
}

.disclaimer {
  background: linear-gradient(135deg, var(--color-black) 0%, var(--color-gray) 100%);
  padding: 2rem;
  border-radius: 10px;
  border-left: 5px solid var(--color-gold);
}

.disclaimer p {
  font-size: 1rem;
  color: rgba(255, 255, 255, 0.9);
  line-height: 1.7;
  margin: 0;
}

.disclaimer strong {
  color: var(--color-gold);
}

@media (max-width: 768px) {
  .policies {
    padding: 4rem 0;
  }

  .section-title {
    font-size: 2rem;
  }

  .policies-content {
    gap: 1.5rem;
  }

  .policy-card {
    padding: 1.5rem;
  }
}
</style>
