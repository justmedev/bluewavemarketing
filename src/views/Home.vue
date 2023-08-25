<template>
  <div style="width: 100%; display: flex; justify-content: center; margin-top: 16px;" ref="logo">
    <img src="../assets/logo.webp" class="logo" alt="BlueWave Logo"/>
  </div>

  <div style="width: 100%; height: 100%; display: flex; justify-content: center; align-items: center">
    <h1>Webseite in Arbeit</h1>
  </div>

<!--  <section id="about">
    <h1>
      Über uns
    </h1>
    <div style="font-size: 20px">
      Wir sind eine leidenschaftliche Gruppe von Social-Media Kennern, wir haben uns
      darauf spezialisiert Ihrer Firma durch Social-Media Kanäle ein möglichst schnelles und großes Wachstum zu bieten.
      Unsere Mission ist es, sie auf ihrem Weg zum Erfolg zu begleiten. Wir glauben daran, dass jedes Unternehmen
      einzigartig ist und eine individuelle Herangehensweise benötigt.
      Innovation treibt uns an. Wir suchen ständig nach neuen Wegen, um unsere Kunden hervorzuheben und ihre Botschaften
      effektiv zu vermitteln.
      Wir sind ein kleines TEam mit viel Expertise auf verschiedenen Gebieten dadurch können wir, Ihre Firma auf vielen
      Online-Plattformen bewerben
      Unsere Vision ist es, nicht nur Marketingkampagnen zu erstellen, sondern Erfolgsgeschichten zu gestalten. Wir sind
      davon überzeugt, dass Ihr Erfolg unser Erfolg ist. Ihre Ziele sind unser Antrieb, und wir sind bereit, die
      Extra-Meile zu gehen, um diese Ziele zu erreichen.
      Bereit, Ihre Marke auf die nächste Stufe zu heben? Wir freuen uns darauf, mit Ihnen zu sprechen. Kontaktieren Sie
      uns noch heute, um mehr zu erfahren.
    </div>
  </section>-->
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
