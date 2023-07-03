<template>
  <div class="cv">
    <div class="text">

      <!-- Timeline -->
      <section>

        <h2>Esperienze professionali</h2>
        <br>
        <div class="timeline" style="max-width: 430px">
          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">Maggio 2022 - presente</div>
            <div class="timeline-content">
              <h3>Jr. Full Stack Web Developer</h3>
              <h4>MyPass</h4>
              <p>Utilizzo e gestione del database aziendale attraverso linguaggio SQL e PHPMyAdmin.</p>
              <p>Sviluppo e personalizzazione dei siti web aziendali basati su piattaforma WordPress.</p>
              <p>Analisi dei dati dei siti web e app iOS/Android utilizzando Google Analytics 4 e monitoraggio delle conversioni tramite Google Tag Manager e Google Ads.</p>
            </div>
          </div>
          
          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">Ottobre 2021 - Aprile 2022</div>
            <div class="timeline-content">
              <h3>Jr. Full Stack Web Developer</h3>
              <h4>Boolean</h4>
              <p>Realizzazione e riproduzione fedele di progetti web app come Netflix, WhatsApp, Spotify, ecc.</p>
              <p>Utilizzo di tecnologie e linguaggi come HTML, SASS, JavaScript, Vue.js, PHP, MySQL e Laravel.</p>
            </div>
          </div>
          
          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">2012 - 2021</div>
            <div class="timeline-content">
              <h3>Insegnante di chitarra</h3>
              <h4>Scuole Medie Statali ad Indirizzo Musicale</h4>
            </div>
          </div>
        </div>

      </section>


      <section style="margin-top: 40px;">
        <h2>Formazione e istruzione</h2>
        <br>

        <div class="timeline" style="width: 430px">
          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">Ottobre 2021 - Aprile 2022</div>
            <div class="timeline-content">
              <h3>Master Full Stack Web Developer</h3>
              <h4>Boolean Careers</h4>
              <p>Master intensivo di 6 mesi con oltre 700 ore (disive in teoria e pratica), lavorando sia in singolo che team e realizzando diversi progetti utilizzando molteplici stack tecnologici come HTML, SASS, JavaScript, Vue.js, PHP, MySQL e Laravel.</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">2014 - 2016</div>
            <div class="timeline-content">
              <h3>Laurea Specialistica</h3>
              <h4>Istituto Superiore di Studi Musicale "V. Bellini" Caltanissetta (CL)</h4>
              <p>Laurea Specialistica in Chitarra con votazione 110/110 e lode.</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">2003 - 2013</div>
            <div class="timeline-content">
              <h3>Laurea Magistrale</h3>
              <h4>Conservatorio di Musica "V. Bellini" - Palermo</h4>
              <p>Laurea Magistrale in Chitarra.</p>
            </div>
          </div>
          
          <div class="timeline-item">
            <div class="rounded"></div>
            <div class="timeline-date">2004 - 2009</div>
            <div class="timeline-content">
              <h3>Maturità Scientifica</h3>
              <h4>Liceo Scientifico "G. Galilei" - Catania</h4>
            </div>
          </div>
        </div>
      </section>




    </div>
  </div>
</template>


<script>
export default {
  name: 'CV',
}
</script>


<style scoped lang="scss">
@import '../style/variables';
@import '../style/generals';

.cv {
  background-color: $second-color;
  min-width: calc(100% - 350px);
  border-radius: 35px;

  // display: flex;
  // justify-content: center;
  // align-items: center;
}

//TIME-LINE
.timeline-item {
  position: relative;
  padding: 20px;
  border-left: 2px solid #2c3e50;
  margin-bottom: 0px;
}

.timeline-date {
  font-weight: bold;
  margin-bottom: 10px;
}

.timeline-content h3 {
  margin: 0;
}

.timeline-content p {
  margin: 10px 0 0;
}

.rounded {
  height: 20px;
  width: 20px;
  background-color: #6e0253;
  border-radius: 50%;
  position: absolute;
  left: -11px
}









.text {
  height: 500px; //IMPORTANTISSIMO DA METTERE ANCHE NEGLI ALTRII!!!!
  text-align: justify;
  padding: 40px;
  opacity: 0;
  animation: appear 0.5s linear 0.5s forwards;
}
@keyframes appear {
  100% {
    opacity: 1;
  }
}




@media (max-width: 1023px) {

  .cv {
    width: 100%;
  }
}
</style>