<template>
  <section id="contato" class="contact">
    <div class="container">

      <h2>Contato</h2>

      <p class="subtitulo">
        Entre em contato comigo através das minhas redes.
      </p>

      <div class="social">

        <!-- EMAIL -->
        <a href="mailto:kaique_batista@outlook.com">
          <span class="icone email">✉</span>
          <span>Email</span>
        </a>

        <!-- CELULAR -->
        <a href="tel:+5511999993623">
          <span class="icone telefone">☎</span>
          <span>Celular</span>
        </a>

        <!-- GITHUB -->
        <a
          href="https://github.com/KaiqueBatista"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i class="devicon-github-original"></i>
          <span>GitHub</span>
        </a>

        <!-- LINKEDIN -->
        <a
          href="https://www.linkedin.com/in/kaique-batista-167aa5349"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i class="devicon-linkedin-plain colored"></i>
          <span>LinkedIn</span>
        </a>

      </div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  width: 100%;

  padding: 100px 8%;

  text-align: center;

  background: #111827;
}

.container {
  width: 100%;
  max-width: 1000px;

  margin: 0 auto;
}

/* =========================
   TÍTULO
========================= */

h2 {
  color: #3B82F6;

  font-size: clamp(30px, 4vw, 40px);

  margin-bottom: 10px;
}

.subtitulo {
  color: #94A3B8;

  font-size: 16px;

  margin-bottom: 40px;
}

/* =========================
   REDES
========================= */

.social {
  display: grid;

  grid-template-columns:
    repeat(4, minmax(0, 1fr));

  gap: 20px;
}

/* =========================
   LINKS
========================= */

.social a {
  min-height: 90px;

  display: flex;

  flex-direction: column;

  justify-content: center;
  align-items: center;

  gap: 10px;

  padding: 20px;

  color: #94A3B8;

  text-decoration: none;

  background: #0F172A;

  border: 1px solid #1F2937;

  border-radius: 12px;

  font-size: 15px;

  transition:
    color 0.3s,
    border-color 0.3s,
    transform 0.3s,
    box-shadow 0.3s;
}

/* ÍCONES */

.social i {
  font-size: 30px;
}

.icone {
  width: 30px;
  height: 30px;

  display: flex;

  align-items: center;
  justify-content: center;

  font-size: 28px;

  line-height: 1;
}

/* HOVER */

.social a:hover {
  color: #3B82F6;

  border-color: #3B82F6;

  transform: translateY(-5px);

  box-shadow:
    0 8px 20px rgba(59, 130, 246, 0.15);
}

/* =========================
   TABLET
========================= */

@media (max-width: 768px) {
  .contact {
    padding: 80px 5%;
  }

  .social {
    grid-template-columns: repeat(2, 1fr);

    gap: 15px;
  }
}

/* =========================
   CELULAR
========================= */

@media (max-width: 480px) {
  .contact {
    padding: 65px 20px;
  }

  .subtitulo {
    font-size: 14px;

    line-height: 1.5;

    margin-bottom: 30px;
  }

  .social {
    grid-template-columns: repeat(2, 1fr);

    gap: 12px;
  }

  .social a {
    min-height: 85px;

    padding: 15px;

    font-size: 14px;
  }

  .social i {
    font-size: 26px;
  }

  .icone {
    font-size: 25px;
  }
}

/* =========================
   CELULAR MUITO PEQUENO
========================= */

@media (max-width: 350px) {
  .contact {
    padding-left: 15px;
    padding-right: 15px;
  }

  .social {
    grid-template-columns: 1fr;
  }
}

/* =========================
   TOUCH
========================= */

@media (hover: none) {
  .social a:hover {
    transform: none;

    box-shadow: none;
  }
}
</style>