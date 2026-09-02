<template>
  <section id="projetos" class="projetos">
    <div class="container">

      <h2>Projetos</h2>

      <p class="subtitulo">
        Alguns dos projetos que desenvolvi durante minha formação e estudos.
      </p>

      <div class="cards">

        <article
          v-for="(projeto, index) in projetos"
          :key="index"
          class="card"
        >

          <!-- IMAGEM -->
          <img
            :src="projeto.imagem"
            :alt="`Imagem do projeto ${projeto.titulo}`"
            loading="lazy"
          >

          <!-- CONTEÚDO -->
          <div class="overlay">

            <h3>
              {{ projeto.titulo }}
            </h3>

            <p>
              {{ projeto.descricao }}
            </p>

            <span class="tecnologias">
              {{ projeto.tecnologias }}
            </span>

            <!-- BOTÕES -->
            <div
              v-if="projeto.github || projeto.demo"
              class="botoes"
            >

              <a
                v-if="projeto.github"
                :href="projeto.github"
                target="_blank"
                rel="noopener noreferrer"
              >
                GitHub
              </a>

              <a
                v-if="projeto.demo"
                :href="projeto.demo"
                target="_blank"
                rel="noopener noreferrer"
              >
                Projeto
              </a>

            </div>

          </div>

        </article>

      </div>

    </div>
  </section>
</template>


<script setup>

const projetos = [

  {
    titulo: "E-commerce",

    descricao:
      "Loja virtual com produtos, categorias e carrinho de compras.",

    tecnologias:
      "React • TypeScript • CSS",

    imagem:
      "/ecommerce.jpg",

    github:
      "https://github.com/KaiqueBatista/Ecommerce",

    demo:
      "https://ecommerce-seven-iota-36.vercel.app/"
  },


  {
    titulo: "Catálogo de Filmes",

    descricao:
      "Aplicação que consome a API TMDB, permitindo buscar filmes e visualizar suas informações.",

    tecnologias:
      "Vue.js • API REST • JavaScript • CSS",

    imagem:
      "/Movie.jpg",

    github:
      "https://github.com/KaiqueBatista/Movie-Finder",

    demo:
      "https://movie-finder-five-xi.vercel.app/"
  },


  {
    titulo: "Dashboard de Estoque",

    descricao:
      "Dashboard para acompanhamento de produtos, estoque e categorias.",

    tecnologias:
      "Vue.js • JavaScript • CSS",

    imagem:
      "/dashboard.jpg",

    github:
      "https://github.com/KaiqueBatista/Dashboard",

    demo:
      "https://dashboard-amber-iota-22.vercel.app/"
  },


  {
    titulo: "Sistema de Chamados",

    descricao:
      "Aplicação CRUD desenvolvida em Vue.js para gerenciamento de chamados.",

    tecnologias:
      "Vue.js • JavaScript • HTML • CSS",

    imagem:
      "/sistema chamado.jpg",

    github:
      "https://github.com/KaiqueBatista/Sistema-de-Chamados",

    demo:
      "https://sistema-de-chamados-mu.vercel.app/"
  },

  {
    titulo: "LanchesJá",

    descricao:
      "Sistema de lanchonete desenvolvido em React, com catálogo de produtos, detalhes dos lanches e carrinho de compras.",

    tecnologias:
      "React • TypeScript • Vite • CSS",

    imagem:
      "/lanchesja.jpg",

    github:
      "https://github.com/KaiqueBatista/LanchesJ-",

    demo:
      "https://lanches-ja.vercel.app/"
  },


  {
    titulo: "Controle Financeiro",

    descricao:
      "Sistema para controle de receitas e despesas pessoais.",

    tecnologias:
      "HTML • JavaScript • CSS",

    imagem:
      "/financeiro.jpg",

    github:
      "https://github.com/KaiqueBatista/Controle-Financeiro",

    demo:
      "https://controle-financeiro-vert-one.vercel.app/"
  }

]

</script>


<style scoped>

/* =====================================================
   SEÇÃO
===================================================== */

.projetos {
  width: 100%;

  padding: 100px 8%;

  background: #0F172A;
}


/* =====================================================
   CONTAINER
===================================================== */

.container {
  width: 100%;

  max-width: 1200px;

  margin: 0 auto;
}


/* =====================================================
   TÍTULO
===================================================== */

.projetos h2 {
  color: #3B82F6;

  font-size: clamp(30px, 4vw, 40px);

  text-align: center;

  margin: 0;
}


/* =====================================================
   SUBTÍTULO
===================================================== */

.subtitulo {
  color: #94A3B8;

  text-align: center;

  font-size: clamp(14px, 2vw, 16px);

  line-height: 1.6;

  margin: 15px auto 50px;

  max-width: 650px;
}


/* =====================================================
   GRID
===================================================== */

.cards {
  display: grid;

  grid-template-columns:
    repeat(3, minmax(0, 1fr));

  gap: 25px;
}


/* =====================================================
   CARD
===================================================== */

.card {
  position: relative;

  width: 100%;

  height: 280px;

  overflow: hidden;

  border-radius: 15px;

  background: #111827;

  border: 1px solid #1F2937;

  cursor: pointer;

  transition:
    transform 0.3s ease,
    border-color 0.3s ease,
    box-shadow 0.3s ease;
}


/* =====================================================
   EFEITO CARD
===================================================== */

.card:hover {
  transform: translateY(-5px);

  border-color: #3B82F6;

  box-shadow:
    0 10px 30px rgba(59, 130, 246, 0.15);
}


/* =====================================================
   IMAGEM
===================================================== */

.card img {
  width: 100%;

  height: 100%;

  display: block;

  object-fit: cover;

  transition:
    transform 0.4s ease;
}


.card:hover img {
  transform: scale(1.08);
}


/* =====================================================
   OVERLAY
===================================================== */

.overlay {
  position: absolute;

  inset: 0;

  background:
    rgba(15, 23, 42, 0.94);

  color: white;

  display: flex;

  flex-direction: column;

  justify-content: center;

  align-items: center;

  text-align: center;

  padding: 20px;

  gap: 8px;

  opacity: 0;

  transition:
    opacity 0.4s ease;
}


.card:hover .overlay {
  opacity: 1;
}


/* =====================================================
   TÍTULO DO PROJETO
===================================================== */

.overlay h3 {
  color: white;

  font-size: clamp(18px, 2vw, 22px);

  line-height: 1.2;

  margin: 0;

  font-weight: 600;
}


/* =====================================================
   DESCRIÇÃO
===================================================== */

.overlay p {
  color: #CBD5E1;

  margin: 0;

  font-size: 14px;

  line-height: 1.45;

  max-width: 95%;
}


/* =====================================================
   TECNOLOGIAS
===================================================== */

.tecnologias {
  color: #3B82F6;

  font-size: 13px;

  line-height: 1.4;

  font-weight: 500;

  max-width: 95%;
}


/* =====================================================
   BOTÕES
===================================================== */

.botoes {
  display: flex;

  gap: 10px;

  justify-content: center;

  align-items: center;

  flex-wrap: wrap;

  margin-top: 10px;
}


/* =====================================================
   LINKS
===================================================== */

.botoes a {
  display: inline-block;

  padding: 9px 16px;

  background: #3B82F6;

  color: white;

  text-decoration: none;

  border-radius: 8px;

  font-size: 14px;

  font-weight: 500;

  transition:
    background 0.3s ease,
    transform 0.3s ease;
}


.botoes a:hover {
  background: #2563EB;

  transform: translateY(-2px);
}


/* =====================================================
   TABLET
===================================================== */

@media (max-width: 900px) {

  .projetos {
    padding: 80px 5%;
  }


  .cards {
    grid-template-columns:
      repeat(2, minmax(0, 1fr));

    gap: 20px;
  }


  .card {
    height: 280px;
  }


  .overlay {
    padding: 20px;
  }


  .overlay p {
    font-size: 13px;
  }

}


/* =====================================================
   CELULAR
===================================================== */

@media (max-width: 600px) {

  .projetos {
    padding: 65px 20px;
  }


  .subtitulo {
    margin-bottom: 30px;
  }


  .cards {
    grid-template-columns: 1fr;

    gap: 20px;
  }


  .card {
    height: 320px;

    cursor: default;
  }


  /*
    No celular o conteúdo fica
    sempre visível.
  */

  .overlay {
    opacity: 1;

    justify-content: flex-end;

    padding: 20px;

    background:
      linear-gradient(
        transparent 0%,
        rgba(15, 23, 42, 0.70) 25%,
        rgba(15, 23, 42, 0.98) 100%
      );
  }


  .overlay h3 {
    font-size: 20px;
  }


  .overlay p {
    font-size: 13px;

    max-width: 100%;
  }


  .tecnologias {
    font-size: 12px;

    max-width: 100%;
  }


  .botoes {
    margin-top: 5px;
  }


  .botoes a {
    padding: 9px 14px;
  }

}


/* =====================================================
   CELULAR PEQUENO
===================================================== */

@media (max-width: 380px) {

  .projetos {
    padding-left: 15px;

    padding-right: 15px;
  }


  .card {
    height: 340px;
  }


  .overlay {
    padding: 15px;
  }


  .overlay h3 {
    font-size: 18px;
  }


  .overlay p {
    font-size: 12px;
  }


  .tecnologias {
    font-size: 11px;
  }


  .botoes a {
    font-size: 12px;

    padding: 8px 12px;
  }

}


/* =====================================================
   TOUCH
===================================================== */

@media (hover: none) {

  .card:hover {
    transform: none;

    box-shadow: none;
  }


  .card:hover img {
    transform: none;
  }


  .botoes a:hover {
    transform: none;
  }

}

</style>