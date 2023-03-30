<template>
  <footer class="footer">
    <div class="footer__content">
      <h1 class="footer__logo">Something</h1>
      <address>
        5534 Somewhere In. The World 22193-10212<br />
        <a class="footer__btn" href="mailto:example@gmail.com">Email Us</a>
      </address>
      <p>&copy; 2019 Something. All rights reserved.</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "MainFooter",
};
</script>

<style>
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

.footer {
  display: flex;
  justify-content: center;
  padding: 30px;
  color: #2f2f2f;
  background-color: var(--main-color);
  flex-shrink: 0;
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

.footer__btn {
  color: #2f2f2f;
  text-decoration: none;
}

.footer p {
  color: black;
  margin: 0;
}
</style>
