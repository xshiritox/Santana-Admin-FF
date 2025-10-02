<template>
  <section id="politicas" class="policies">
    <div class="container">
      <h2 class="section-title">Políticas y Términos</h2>
      <div class="title-underline"></div>

      <div class="policies-content">
        <div class="policy-card">
          <div class="policy-icon" aria-hidden="true">
            <!-- Outline Clipboard -->
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <rect x="7" y="4" width="10" height="16" rx="2" ry="2" fill="none"/>
              <path d="M9 4h6v3H9V4Z" fill="none"/>
              <path d="M9 10h6M9 14h6" fill="none"/>
            </svg>
          </div>
          <h3 class="policy-title">Rol de Intermediario</h3>
          <p class="policy-text">
            <strong>Importante:</strong> No vendo cuentas directamente. Mi función es actuar como
            <strong>intermediario</strong> entre compradores y vendedores, garantizando
            que las transacciones se realicen de forma segura y transparente. 
          </p>
        </div>

        <div class="policy-card">
          <div class="policy-icon" aria-hidden="true">
            <!-- Outline Scales of Justice -->
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <path d="M12 3v3m0 0 5 3m-5-3-5 3" fill="none"/>
              <path d="M7 9l-3 5h6L7 9Z" fill="none"/>
              <path d="M17 9l-3 5h6l-3-5Z" fill="none"/>
              <path d="M12 6v12M9 21h6" fill="none"/>
            </svg>
          </div>
          <h3 class="policy-title">Aviso Legal</h3>
          <p class="policy-text">
            No me hago responsable de cuentas que incumplan las normas de Garena o Free Fire.
            Es responsabilidad del comprador asegurar que la cuenta esté libre de sanciones,
            restricciones o violaciones de términos de servicio.
          </p>
        </div>

        <div class="policy-card">
          <div class="policy-icon" aria-hidden="true">
            <!-- Outline Lock -->
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <rect x="5" y="11" width="14" height="9" rx="2" ry="2" fill="none"/>
              <path d="M8 11V8a4 4 0 1 1 8 0v3" fill="none"/>
              <circle cx="12" cy="15" r="1" fill="none"/>
            </svg>
          </div>
          <h3 class="policy-title">Seguridad y Transparencia</h3>
          <p class="policy-text">
            Todas las transacciones son verificadas antes de proceder. Solicito información
            completa de la cuenta y coordino directamente con ambas partes para asegurar que
            todo esté en orden antes de finalizar cualquier operación.
          </p>
        </div>

        <div class="policy-card">
          <div class="policy-icon" aria-hidden="true">
            <!-- Outline Briefcase -->
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" role="img" focusable="false">
              <rect x="3" y="7" width="18" height="12" rx="2" ry="2" fill="none"/>
              <path d="M9 7V5a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2v2" fill="none"/>
              <path d="M3 12h18" fill="none"/>
              <path d="M12 12v2" fill="none"/>
            </svg>
          </div>
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
  margin: 0 auto 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 3rem;
  height: 3rem;
}

.policy-icon svg {
  width: 100%;
  height: 100%;
  fill: none;
  stroke: var(--color-gold);
  stroke-width: 2;
  stroke-linecap: round;
  stroke-linejoin: round;
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
