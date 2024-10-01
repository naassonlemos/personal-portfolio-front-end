<template>
  <div>
    <header>
      <nav>
        <a href="/">Home</a>
        <a href="/about">Sobre</a>
      </nav>
    </header>

    <NuxtPage />

    <footer>
      <p>© 2024 Meu Portfólio</p>
    </footer>
  </div>
</template>

<script setup></script>

<style scoped lang="scss">
header {
  background: #333;
  color: white;
  padding: 1rem;
  text-align: center;
}

footer {
  background: #333;
  color: white;
  text-align: center;
  padding: 1rem;
  position: fixed;
  width: 100%;
  bottom: 0;
}
</style>
