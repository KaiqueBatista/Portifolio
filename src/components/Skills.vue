<template>
  <section id="skills" class="skills">
    <div class="container">
      <h2>Habilidades</h2>

      <p class="subtitulo">
        Tecnologias que utilizo no desenvolvimento de aplicações web.
      </p>

      <div class="grid">

        <!-- FRONT-END -->
        <div class="card">
          <i class="devicon-html5-plain colored"></i>
          <p>HTML</p>
        </div>

        <div class="card">
          <i class="devicon-css3-plain colored"></i>
          <p>CSS</p>
        </div>

        <div class="card">
          <i class="devicon-javascript-plain colored"></i>
          <p>JavaScript</p>
        </div>

        <div class="card">
          <i class="devicon-vuejs-plain colored"></i>
          <p>Vue.js</p>
        </div>

        <div class="card">
          <i class="devicon-react-original colored"></i>
          <p>React.js</p>
        </div>

        <div class="card">
          <i class="devicon-typescript-plain colored"></i>
          <p>TypeScript</p>
        </div>

        <!-- API -->
        <div class="card">
          <i class="devicon-postman-plain colored"></i>
          <p>API REST</p>
        </div>

        <div class="card">
          <i class="devicon-axios-plain"></i>
          <p>Axios</p>
        </div>

        <!-- FERRAMENTAS -->
        <div class="card">
          <i class="devicon-git-plain colored"></i>
          <p>Git</p>
        </div>

        <div class="card">
          <i class="devicon-github-original"></i>
          <p>GitHub</p>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
.skills {
  width: 100%;

  padding: 100px 8%;

  background: #0F172A;

  text-align: center;
}

.container {
  width: 100%;
  max-width: 1100px;

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

  font-size: clamp(14px, 2vw, 16px);

  line-height: 1.6;

  margin-bottom: 50px;
}

/* =========================
   GRID
========================= */

.grid {
  display: grid;

  grid-template-columns:
    repeat(auto-fit, minmax(160px, 1fr));

  gap: 20px;
}

/* =========================
   CARD
========================= */

.card {
  min-height: 150px;

  display: flex;
  flex-direction: column;

  justify-content: center;
  align-items: center;

  gap: 12px;

  padding: 25px 20px;

  background: #111827;

  border: 1px solid transparent;

  border-radius: 12px;

  cursor: pointer;

  transition:
    transform 0.3s,
    border-color 0.3s,
    box-shadow 0.3s;
}

/* ÍCONES */

.card i {
  font-size: 48px;

  line-height: 1;

  transition: transform 0.3s;
}

/* TEXTO */

.card p {
  color: #E2E8F0;

  font-size: 16px;

  font-weight: 500;
}

/* HOVER */

.card:hover {
  transform: translateY(-5px);

  border-color: #3B82F6;

  box-shadow:
    0 10px 25px rgba(59, 130, 246, 0.25);
}

.card:hover i {
  transform: scale(1.1);
}

/* =========================
   TABLET
========================= */

@media (max-width: 768px) {
  .skills {
    padding: 80px 5%;
  }

  .grid {
    grid-template-columns:
      repeat(3, minmax(120px, 1fr));

    gap: 15px;
  }

  .card {
    min-height: 140px;

    padding: 20px 15px;
  }

  .card i {
    font-size: 42px;
  }
}

/* =========================
   CELULAR
========================= */

@media (max-width: 600px) {
  .skills {
    padding: 65px 20px;
  }

  .subtitulo {
    margin-bottom: 30px;
  }

  .grid {
    grid-template-columns: repeat(2, 1fr);

    gap: 12px;
  }

  .card {
    min-height: 130px;

    padding: 20px 10px;
  }

  .card i {
    font-size: 40px;
  }

  .card p {
    font-size: 14px;
  }
}

/* =========================
   CELULAR PEQUENO
========================= */

@media (max-width: 380px) {
  .skills {
    padding-left: 15px;
    padding-right: 15px;
  }

  .grid {
    gap: 10px;
  }

  .card {
    min-height: 120px;
  }

  .card i {
    font-size: 36px;
  }
}

/* =========================
   TOUCH
========================= */

@media (hover: none) {
  .card:hover {
    transform: none;

    box-shadow: none;

    border-color: transparent;
  }

  .card:hover i {
    transform: none;
  }
}
</style>