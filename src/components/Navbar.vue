<script setup>
import { ref } from 'vue'

const menuAberto = ref(false)

const fecharMenu = () => {
  menuAberto.value = false
}
</script>

<template>
  <header class="navbar">
    <a href="#home" class="logo" @click="fecharMenu">
      Kaique Oliveira Batista
    </a>

    <!-- Botão mobile -->
    <button
      class="menu-btn"
      :class="{ ativo: menuAberto }"
      @click="menuAberto = !menuAberto"
      aria-label="Abrir menu"
      :aria-expanded="menuAberto"
    >
      <span></span>
      <span></span>
      <span></span>
    </button>

    <nav :class="{ aberto: menuAberto }">
      <a href="#home" @click="fecharMenu">Home</a>
      <a href="#projetos" @click="fecharMenu">Projetos</a>
      <a href="#skills" @click="fecharMenu">Habilidades</a>
      <a href="#sobre" @click="fecharMenu">Sobre</a>
      <a href="#formacao" @click="fecharMenu">Formação</a>
      <a href="#contato" @click="fecharMenu">Contato</a>
    </nav>
  </header>
</template>

<style scoped>
.navbar {
  width: 100%;
  height: 80px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 0 clamp(20px, 8%, 120px);

  position: fixed;
  top: 0;
  left: 0;

  z-index: 1000;

  background: rgba(17, 24, 39, 0.85);
  backdrop-filter: blur(10px);

  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}

.logo {
  color: #3B82F6;
  font-size: clamp(20px, 2vw, 28px);
  font-weight: 700;
  text-decoration: none;
  white-space: nowrap;
}

nav {
  display: flex;
  align-items: center;
  gap: clamp(15px, 2.5vw, 30px);
}

nav a {
  color: white;
  text-decoration: none;
  font-size: 15px;
  transition: 0.3s;
  white-space: nowrap;
}

nav a:hover {
  color: #3B82F6;
}

/* Botão inicialmente escondido */
.menu-btn {
  display: none;

  width: 42px;
  height: 42px;

  padding: 8px;

  border: none;
  background: transparent;

  cursor: pointer;

  flex-direction: column;
  justify-content: center;
  gap: 5px;
}

.menu-btn span {
  display: block;

  width: 26px;
  height: 3px;

  border-radius: 3px;

  background: white;

  transition: 0.3s;
}

/* TABLET / CELULAR */
@media (max-width: 900px) {
  .navbar {
    height: 70px;
    padding: 0 20px;
  }

  .logo {
    font-size: 19px;
  }

  .menu-btn {
    display: flex;
  }

  nav {
    position: absolute;

    top: 70px;
    left: 0;

    width: 100%;

    padding: 20px;

    display: none;
    flex-direction: column;
    align-items: center;

    gap: 20px;

    background: rgba(17, 24, 39, 0.97);
    backdrop-filter: blur(10px);

    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  }

  nav.aberto {
    display: flex;
  }

  nav a {
    font-size: 16px;
  }
}

/* CELULARES PEQUENOS */
@media (max-width: 400px) {
  .navbar {
    padding: 0 15px;
  }

  .logo {
    font-size: 16px;
  }
}

/* Animação do hambúrguer */
.menu-btn.ativo span:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}

.menu-btn.ativo span:nth-child(2) {
  opacity: 0;
}

.menu-btn.ativo span:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}
</style>