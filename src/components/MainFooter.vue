<template>
  <div class="page-container">
    <div class="content-wrap">
      <div class="about main-content">
        <footer class="footer">
          <div class="footer__content">
            <h1 class="footer__logo">Korean Ramen Epicerie Asiatique Montpellier</h1>
            <address>
              114 Av. de Toulouse, 34070 Montpellier<br />
              <RouterLink to="/contact" class="action_btn">Contactez nous</RouterLink>
            </address>
            <a href="https://github.com/Loke-60000">Website by Lokman</a>
          </div>
        </footer>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "MainFooter",
};
</script>
<style>
.page-container {
  display: flex;
  flex-direction: column;
  min-height: 25vh;
  position: relative;
}

.content-wrap {
  flex: 1;
}

.footer {
  display: flex;
  justify-content: center;
  padding: 30px;
  color: #2f2f2f;
  background-color: var(--main-color);
  flex-shrink: 0;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
}

h1 {
  color: black;
}

:any-link {
  color: black;
}

html,
body {
  height: 100%;
  margin: 0;
  display: flex;
  flex-direction: column;
  font-size: 14px;
  background-color: #f4f4f4;
}

body {
  flex: 1 0 auto;
}

.footer__content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer__logo {
  font-weight: 400;
  font-size: 1.5rem;
  text-transform: lowercase;
  margin-bottom: 1em;
}

.footer address {
  font-style: normal;
  color: black;
  text-align: center;
  margin-bottom: 1em;
}

.action_btn {
  color: #2f2f2f;
  text-decoration: none;
}

.footer p {
  color: black;
  margin: 0;
}

/* Add the following media query for responsiveness */
@media (max-width: 768px) {
  .footer__content {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 15px;
  }

  .footer__logo {
    font-size: 1.2rem;
  }

  .footer address {
    font-size: 0.9rem;
  }

  .action_btn {
    font-size: 0.9rem;
  }

  .footer a {
    font-size: 0.9rem;
  }
}
</style>
