<template>
  <footer class="footer">
    <div class="container">
      <p class="copy">
        © 2026 Kaique Oliveira Batista
      </p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  width: 100%;

  background: #0B1220;

  padding: 40px 8%;

  text-align: center;

  border-top: 1px solid #1F2937;
}

.container {
  width: 100%;
  max-width: 1000px;

  margin: 0 auto;
}

.copy {
  color: #64748B;

  font-size: 13px;

  line-height: 1.6;
}

/* TABLET */
@media (max-width: 768px) {
  .footer {
    padding: 35px 5%;
  }

  .copy {
    font-size: 12px;
  }
}

/* CELULAR */
@media (max-width: 480px) {
  .footer {
    padding: 30px 20px;
  }

  .copy {
    font-size: 11px;
  }
}
</style>