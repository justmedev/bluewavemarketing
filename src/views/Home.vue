<template>
  <div style="width: 100%; display: flex; justify-content: center; margin-top: 16px;" ref="logo">
    <img src="../assets/logo.webp" class="logo" alt="BlueWave Logo"/>
  </div>
  <!--

    <div style="width: 100%; height: 100%; display: flex; justify-content: center; align-items: center">
      <h1>Webseite in Arbeit</h1>
    </div>
  -->

  <section id="about">
    <h1>
      Was wir bieten
    </h1>
    <div style="font-size: 20px">
      Wir übernehmen Ihr komplettes Social-Media-Management auf verschiedensten Plattformen: Instagram, Tiktok, Facebook
      und X (Twitter). Des weiteren bieten wir Google Ads Kampagnen und Google Ads Management. Wir editieren Ihre
      Poolbau & fertigstellungs-Bilder und Videos professionell, modern und trendy um die Reichweite zu erweitern. Falls
      Sie Wünsche haben, richten wir uns danach und erstellen Ihre Social-Media präsens persönlich nach Ihren Vorstellungen.
    </div>
  </section>
</template>

<script setup lang="ts">

</script>

<style scoped>
.logo {
  width: 40%;
  transition: width 250ms ease-in-out;
}

@media only screen and (max-width: 850px) {
  .logo {
    margin-top: 10px;
    width: 60%;
  }
}

@media only screen and (max-width: 600px) {
  .logo {
    margin-top: 10px;
    width: 70%;
  }
}
</style>
