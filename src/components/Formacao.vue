<template>
  <section id="formacao" class="formacao">
    <h2>Formação Acadêmica</h2>

    <div class="container">

      <!-- GRADUAÇÃO -->
      <div class="card destaque">
        <h3>Graduação em Análise e Desenvolvimento de Sistemas</h3>
        <p>Universidade Anhanguera</p>
        <span>07/2024 - 01/2027</span>
      </div>

      <!-- TÉCNICO -->
      <div class="card">
        <h3>Curso Técnico em Comunicação Visual</h3>
        <p>Colégio e Faculdade Drummond Alvorada</p>
        <span>2013 - 2014</span>
      </div>

      <!-- CURSOS -->
      <h2 class="subtitulo">Cursos Complementares</h2>

      <div class="card">
        <h3>JavaScript</h3>
        <p>Alura</p>
        <a
          href="https://www.alura.com.br"
          target="_blank"
          rel="noopener noreferrer"
        >
          Ver instituição
        </a>
      </div>

      <div class="card">
        <h3>Python</h3>
        <p>Hashtag Programação</p>
        <a
          href="https://www.hashtagtreinamentos.com"
          target="_blank"
          rel="noopener noreferrer"
        >
          Ver instituição
        </a>
      </div>

      <div class="card">
        <h3>FullStack</h3>
        <p>Hashtag Programação</p>
        <a
          href="https://www.hashtagtreinamentos.com"
          target="_blank"
          rel="noopener noreferrer"
        >
          Ver instituição
        </a>
      </div>

      <div class="card">
        <h3>Excel</h3>
        <p>ENAP</p>
        <a
          href="https://www.enap.gov.br"
          target="_blank"
          rel="noopener noreferrer"
        >
          Ver instituição
        </a>
      </div>

    </div>
  </section>
</template>

<style scoped>
.formacao {
  width: 100%;

  padding: 100px 8%;

  background: #0F172A;

  text-align: center;
}

.formacao > h2 {
  color: #3B82F6;

  font-size: clamp(30px, 4vw, 40px);

  margin-bottom: 40px;
}

/* =========================
   GRID
========================= */

.container {
  width: 100%;
  max-width: 1000px;

  margin: 0 auto;

  display: grid;

  grid-template-columns: repeat(2, minmax(0, 1fr));

  gap: 20px;
}

/* =========================
   SUBTÍTULO
========================= */

.subtitulo {
  grid-column: 1 / -1;

  margin-top: 40px;
  margin-bottom: 0;

  color: #94A3B8;

  font-size: clamp(24px, 3vw, 28px);
}

/* =========================
   CARD
========================= */

.card {
  width: 100%;

  background: #111827;

  padding: 25px;

  border-radius: 12px;

  border: 1px solid #1F2937;

  text-align: left;

  transition:
    transform 0.3s,
    border-color 0.3s,
    box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-5px);

  border-color: #3B82F6;

  box-shadow:
    0 10px 25px rgba(59, 130, 246, 0.2);
}

/* =========================
   DESTAQUE
========================= */

.destaque {
  border-left: 4px solid #3B82F6;
}

/* =========================
   TEXTOS
========================= */

.card h3 {
  color: #E2E8F0;

  font-size: 18px;

  line-height: 1.4;

  margin-bottom: 8px;
}

.card p {
  color: #94A3B8;

  font-size: 15px;

  line-height: 1.5;

  margin-bottom: 5px;
}

.card span {
  color: #3B82F6;

  font-size: 14px;
}

/* =========================
   LINKS
========================= */

.card a {
  display: inline-block;

  margin-top: 10px;

  color: #3B82F6;

  text-decoration: none;

  font-size: 14px;

  transition: 0.3s;
}

.card a:hover {
  color: #60A5FA;
}

/* =========================
   TABLET
========================= */

@media (max-width: 768px) {
  .formacao {
    padding: 80px 5%;
  }

  .container {
    gap: 16px;
  }

  .card {
    padding: 22px;
  }
}

/* =========================
   CELULAR
========================= */

@media (max-width: 600px) {
  .formacao {
    padding: 65px 20px;
  }

  .container {
    grid-template-columns: 1fr;

    gap: 15px;
  }

  .subtitulo {
    grid-column: 1;

    margin-top: 30px;
  }

  .card {
    padding: 20px;
  }

  .card h3 {
    font-size: 17px;
  }

  .card p {
    font-size: 14px;
  }

  .card a {
    padding: 5px 0;
  }
}

/* =========================
   TOUCH
========================= */

@media (hover: none) {
  .card:hover {
    transform: none;

    box-shadow: none;
  }
}
</style>