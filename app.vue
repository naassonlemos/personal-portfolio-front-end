<template>
  <div id="app">
    <header>
      <nav>
        <div class="logo">Meu Portfólio</div>
        <ul>
          <li><a href="/">Início</a></li>
          <li><a href="#about">Sobre Mim</a></li>
          <li><a href="#projects">Projetos</a></li>
          <li><a href="#contact">Contato</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <NuxtPage />
    </main>

    <footer>
      <p>© 2024 Meu Nome. Todos os direitos reservados.</p>
    </footer>
  </div>
</template>

<script setup></script>

<style  lang="scss">
*,
*::before,
*::after {
  padding: 0;
  box-sizing: border-box;
  max-width: 100%;

}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  max-width: 100%;

}

header {
  position: fixed;
  background-color: #00465F;
  color: white;
  width: 100%;
  top: 0;
  z-index: 100;
  max-width: 100%;

  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 100%;
    overflow: hidden;
    padding: 1rem;


    .logo {
      font-size: 1.5rem;
      font-weight: bold;
    }

    ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
      flex-wrap: wrap;

      li {
        a {
          color: white;
          text-decoration: none;
          font-weight: 500;
          transition: color 0.3s;

          &:hover {
            color: #64B5CE;
          }
        }
      }
    }
  }
}

main {
  flex: 1;
  margin-top: 80px;
}

footer {
  background-color: #002A3A;
  color: white;
  text-align: center;
  padding: 1rem;
}
</style>
