<template>
  <div>
    <section class="hero">
      <div class="content">
        <h1>Olá, eu sou <span>Seu Nome</span></h1>
        <p>Desenvolvedor Web | Designer Gráfico | Freelancer</p>
        <a href="#contact" class="btn">Entre em Contato</a>
      </div>
    </section>

    <section id="about" class="about">
      <h2>Sobre Mim</h2>
      <p>
        Sou um desenvolvedor apaixonado por criar soluções web inovadoras. Com experiência em diversas tecnologias, busco sempre aprimorar minhas habilidades e entregar projetos de alta qualidade.
      </p>
    </section>

    <section id="projects" class="projects">
      <h2>Projetos</h2>
      <div class="project-list">
        <div class="project-item">
          <!-- <img src="project1.jpg" alt="Projeto 1"> -->
          <h3>Projeto 1</h3>
          <p>Descrição breve do projeto 1.</p>
        </div>
      </div>
    </section>

    <section id="contact" class="contact">
      <h2>Contato</h2>
      <form @submit.prevent="submitForm">
        <input type="text" placeholder="Seu Nome" required>
        <input type="email" placeholder="Seu Email" required>
        <textarea placeholder="Sua Mensagem" required></textarea>
        <button type="submit">Enviar Mensagem</button>
      </form>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const submitForm = () => {
  alert('Mensagem enviada com sucesso!');
};
</script>

<style scoped lang="scss">
/* Seção Hero */
.hero {
  background: linear-gradient(135deg, #318FAC, #64B5CE);
  color: white;
  padding: 150px 0;
  text-align: center;
  position: relative;
  overflow: hidden;

  .content {
    position: relative;
    z-index: 1;

    h1 {
      font-size: 3rem;
      margin-bottom: 1rem;

      span {
        color: #E0EFF6;
      }
    }

    p {
      font-size: 1.5rem;
      margin-bottom: 2rem;
    }

    .btn {
      background-color: #002A3A;
      color: white;
      padding: 0.75rem 1.5rem;
      text-decoration: none;
      border-radius: 50px;
      transition: background-color 0.3s;

      &:hover {
        background-color: #00465F;
      }
    }
  }

  /* Animação */
  &::before {
    content: '';
    position: absolute;
    top: -50px;
    left: -50px;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle at center, rgba(255, 255, 255, 0.1), transparent);
    animation: rotate 20s infinite linear;
  }

  @keyframes rotate {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }
}

/* Seção Sobre Mim */
.about {
  background-color: #ECF7FB;
  padding: 80px 20px;
  text-align: center;

  h2 {
    font-size: 2.5rem;
    color: #00465F;
    margin-bottom: 1rem;
  }

  p {
    max-width: 800px;
    margin: 0 auto;
    font-size: 1.2rem;
    line-height: 1.6;
    color: #002A3A;
  }
}

/* Seção Projetos */
.projects {
  padding: 80px 20px;
  text-align: center;

  h2 {
    font-size: 2.5rem;
    color: #00465F;
    margin-bottom: 2rem;
  }

  .project-list {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;

    .project-item {
      background-color: #F3F6F9;
      padding: 1rem;
      border-radius: 10px;
      width: calc(33.333% - 2rem);
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);

      img {
        max-width: 100%;
        border-radius: 10px;
      }

      h3 {
        margin-top: 1rem;
        color: #002A3A;
      }

      p {
        color: #00465F;
      }
    }
  }
}

/* Seção Contato */
.contact {
  background-color: #E0EFF6;
  padding: 80px 20px;
  text-align: center;

  h2 {
    font-size: 2.5rem;
    color: #00465F;
    margin-bottom: 2rem;
  }

  form {
    max-width: 600px;
    margin: 0 auto;

    input,
    textarea {
      width: 100%;
      padding: 0.75rem;
      margin-bottom: 1rem;
      border: 1px solid #BEDCEB;
      border-radius: 5px;
    }

    button {
      background-color: #00465F;
      color: white;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      transition: background-color 0.3s;

      &:hover {
        background-color: #002A3A;
      }
    }
  }
}
</style>
