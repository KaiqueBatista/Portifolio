<template>
  <section id="sobre" class="sobre">
    <div class="container">
      <h2>Sobre Mim</h2>

      <div class="textos">
        <p>
          Sou estudante de Análise e Desenvolvimento de Sistemas e venho construindo minha trajetória na tecnologia com foco em Front-End. 
          Gosto de transformar ideias em interfaces funcionais e agradáveis de usar.
        </p>

        <p>
          Tenho buscado consolidar meus conhecimentos por meio de projetos próprios,
          aplicando conceitos como consumo de APIs, manipulação de dados,
          componentes reutilizáveis e interfaces responsivas.
        </p>

        <p>
          Meu objetivo é conquistar minha primeira oportunidade como Desenvolvedor
          Front-End e continuar evoluindo profissionalmente.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.sobre {
  width: 100%;
  background: #111827;
  padding: 100px 8%;
}

.container {
  width: 100%;
  max-width: 1100px;
  margin: 0 auto;
}

h2 {
  color: #3B82F6;
  font-size: clamp(30px, 4vw, 38px);
  margin-bottom: 35px;
}

.textos {
  display: flex;
  flex-direction: column;
  gap: 25px;
}

p {
  color: #CBD5E1;
  font-size: clamp(16px, 2vw, 20px);
  line-height: 1.8;
  text-align: justify;
}

/* TABLET */
@media (max-width: 768px) {
  .sobre {
    padding: 80px 5%;
  }

  h2 {
    margin-bottom: 25px;
  }

  p {
    text-align: left;
    line-height: 1.7;
  }

  .textos {
    gap: 20px;
  }
}

/* CELULAR */
@media (max-width: 480px) {
  .sobre {
    padding: 65px 20px;
  }

  h2 {
    font-size: 30px;
    margin-bottom: 20px;
  }

  p {
    font-size: 15px;
    line-height: 1.7;
  }

  .textos {
    gap: 18px;
  }
}
</style>