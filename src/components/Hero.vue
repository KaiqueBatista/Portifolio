
<template>
  <section id="home" class="hero">
    <div class="foto">
      <img
        src="/perfil.jpeg"
        alt="Foto de perfil de Kaique Oliveira Batista"
        fetchpriority="high"
      >
    </div>

    <div class="texto">
      <p>Olá, eu sou</p>

      <h1>Kaique Batista</h1>

      <h2>Desenvolvedor Front-End Júnior</h2>

      <span>
        Desenvolvo aplicações web com React, Vue.js, JavaScript,
        TypeScript e Tailwind CSS, criando interfaces responsivas
        e funcionais.
      </span>

      <div class="botoes">
        <a
          href="/Curriculo%20-%20Kaique%20Oliveira%20Batista%20dev%20jr.pdf"
          class="botao principal"
          download
        >
          Download CV
        </a>

        <a href="#projetos" class="botao secundario">
          Ver projetos
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: calc(100vh - 80px);
  display: flex;
  justify-content: center;
  align-items: center;
  gap: clamp(40px, 6vw, 80px);
  padding: 80px 8%;
  overflow: hidden;
}

.texto {
  width: 50%;
  max-width: 650px;
}

.texto > p {
  color: #94A3B8;
  font-size: clamp(18px, 2vw, 22px);
}

.texto h1 {
  color: white;
  font-size: clamp(50px, 6vw, 70px);
  margin: 10px 0;
  line-height: 1.1;
}

.texto h2 {
  color: #CBD5E1;
  font-size: clamp(18px, 2vw, 24px);
  font-weight: 600;
  margin-bottom: 15px;
}

.texto span {
  display: block;
  color: #3B82F6;
  font-size: clamp(16px, 1.8vw, 22px);
  line-height: 1.6;
}

.botoes {
  display: flex;
  gap: 20px;
  margin-top: 40px;
}

.botao {
  display: inline-block;
  padding: 14px 28px;
  border-radius: 8px;
  text-decoration: none;
  font-size: 16px;
  font-weight: 500;
  transition: background 0.3s, color 0.3s, transform 0.3s;
  text-align: center;
}

.botao:focus-visible {
  outline: 2px solid white;
  outline-offset: 4px;
}

.botao.principal {
  background: #3B82F6;
  color: white;
}

.botao.principal:hover {
  background: #2563EB;
  transform: translateY(-2px);
}

.botao.secundario {
  background: transparent;
  border: 1px solid #3B82F6;
  color: #3B82F6;
}

.botao.secundario:hover {
  background: #3B82F6;
  color: white;
  transform: translateY(-2px);
}

.foto {
  width: 40%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.foto img {
  width: min(350px, 100%);
  aspect-ratio: 1 / 1;
  object-fit: cover;
  border-radius: 50%;
  border: 5px solid #3B82F6;
  box-shadow: 0 0 40px rgba(59, 130, 246, 0.25);
}

@media (max-width: 900px) {
  .hero {
    gap: 30px;
    padding: 70px 5%;
  }

  .texto {
    width: 55%;
  }

  .foto {
    width: 45%;
  }

  .foto img {
    width: min(300px, 100%);
  }
}

@media (max-width: 768px) {
  .hero {
    min-height: auto;
    flex-direction: column;
    text-align: center;
    gap: 45px;
    padding: 60px 20px 80px;
  }

  .foto {
    order: 1;
    width: 100%;
  }

  .texto {
    order: 2;
    width: 100%;
    max-width: 600px;
  }

  .foto img {
    width: min(280px, 75vw);
  }

  .texto h1 {
    font-size: clamp(45px, 14vw, 65px);
  }

  .texto h2 {
    font-size: 18px;
  }

  .texto span {
    font-size: 16px;
  }

  .botoes {
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 30px;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 45px 18px 60px;
    gap: 35px;
  }

  .foto img {
    width: 220px;
  }

  .texto > p {
    font-size: 17px;
  }

  .texto h1 {
    font-size: 48px;
  }

  .texto h2 {
    font-size: 16px;
    line-height: 1.4;
  }

  .texto span {
    font-size: 15px;
    line-height: 1.5;
  }

  .botoes {
    flex-direction: column;
    width: 100%;
    gap: 12px;
  }

  .botao {
    width: 100%;
  }
}

@media (prefers-reduced-motion: reduce) {
  .botao {
    transition: none;
  }

  .botao:hover {
    transform: none;
  }
}
</style>
