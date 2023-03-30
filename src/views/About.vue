<template>
  <div class="about">
    <div class="content">
      <h1>À propos</h1>
      <p>
        Bienvenue dans notre épicerie spécialisée en produits asiatiques ! Nous sommes fiers de vous proposer une vaste gamme d'ingrédients, de snacks, de plats préparés, de desserts et de boissons provenant de divers pays d'Asie. Vous y trouverez un large choix de ramen, sauces, épices, thés et autres spécialités culinaires pour éveiller vos papilles et vous transporter au cœur de l'Asie.
      </p>
      <p>
        Profitez également de notre espace de restauration chaleureux et accueillant, où vous pourrez savourer nos délicieux plats asiatiques préparés avec soin par notre équipe de cuisiniers expérimentés. Que vous souhaitiez goûter à un curry épicé, un bento savoureux ou un dessert exotique, il y en a pour tous les goûts et toutes les envies.
      </p>
      <p>
        Notre personnel amical et compétent se fera un plaisir de vous guider à travers notre sélection de produits et de vous fournir des conseils sur la préparation de plats traditionnels. N'hésitez pas à nous poser des questions ou à demander des recommandations pour que votre expérience soit à la hauteur de vos attentes.
      </p>
    </div>
    <div class="map-container">
      <div>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2889.536584403017!2d3.8595915154958695!3d43.59536807912339!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x12b6afade268f367%3A0xbf37a04d5a3b48a2!2sKorean%20Ramen%20%C3%A9picerie%20asiatique%20Montpellier!5e0!3m2!1sfr!2sfr!4v1680148101039!5m2!1sfr!2sfr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
      <div class="address-container">
        <p>114 Av. de Toulouse, 34070 Montpellier</p>
        <a href="tel:0630747821" class="phone-btn">0630747821</a>
        <div class="opening-hours">
          <p>lundi: 10:00–20:00</p>
          <p>mardi: 10:00–20:00</p>
          <p>mercredi: 10:00–20:00</p>
          <p>jeudi: 10:00–20:00</p>
          <p>vendredi: 10:00–20:00</p>
          <p>samedi: 10:00–20:00</p>
          <p>dimanche: 10:00–20:00</p>
        </div>
      </div>
    </div>
  </div>
  <MainFooter/>
</template>
<script>

export default {
  name: "About",
  // components: {MainFooter},
};

</script>

<style scoped>
.about {
  text-align: center;
  background-color: white;
  overflow: hidden;
  padding-bottom: 2rem;
}
.about h1, p {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: black;
  font-size: medium;
}
.content{
  padding-top: 2rem;
  margin: 0 10%;
  width: 80vw;
  max-width: 100%;
  box-sizing: border-box;
}
.map-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  margin-top: 100px;
}

.address-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.opening-hours p {
  margin: 0.25rem 0;
}

/* Add a media query for mobile devices */
@media (max-width: 768px) {
  .content {
    padding-top: 1rem;
    margin: 0 5%;
  }

  .about h1, p {
    font-size: 1.5rem;
  }

  .map-container {
    flex-direction: column;
  }

  .address-container {
    margin-top: 1rem;
  }

  .opening-hours p {
    font-size: 0.8rem;
  }

  iframe {
    width: 100%;
    height: 300px;
  }
}
</style>