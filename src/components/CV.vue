<template>
  <div id="cv">
    <div class="header-decoration">
      <div class="left-section"></div>
      <div class="right-section"></div>
    </div>
    <header>
      <div class="profile-pic">
        <img src="@/assets/img/moi32opti.jpg" alt="Photo de moi" />
      </div>
      <img
        class="rotat"
        src="@/assets/img/PAQrenderopti2.png"
        alt="Paille en queue"
      />
      <div class="profile-info">
        <h1>Luc FERRO</h1>
        <h2>Développeur web</h2>
        <ul class="profile-contacts">
          <li>
            <i class="fas fa-baby-carriage"></i>
            <p>Né le 15/05/1997</p>
          </li>
          <li>
            <i class="fas fa-car"></i>
            <p>Permis B, véhiculé</p>
          </li>
          <li>
            <i class="fas fa-home"></i>
            <p>
              34 Rue des pipots <br />
              62200 Boulogne sur mer
            </p>
          </li>
        </ul>
      </div>
      <div class="logo">
        <img src="@/assets/img/render.png" alt="Logo de la promo" />
      </div>
    </header>
    <section class="main-content">
      <div class="left-section">
        <div class="language">
          <ul>
            <li><h3>Langages</h3></li>
            <li>
              <p>
                <em>Bureautique:</em><br />
                Word, Excel, PowerPoint, Geogebra, Scratch, Scilab, LaTeX
              </p>
            </li>
            <li>
              <p>
                <em>Développeur web:</em><br />
                HTML, CSS, PHP, JavaScript, SQL, Python
              </p>
            </li>
            <li>
              <p>
                <em>Langues:</em><br />
                Anglais (C1), Espagnol (A2)
              </p>
            </li>
          </ul>
        </div>
        <div class="softskills">
          <ul>
            <li><h3>Soft skills</h3></li>
            <li>Autonomie</li>
            <li>Curiosité</li>
            <li>Flexibilité</li>
            <li>Travail en équipe</li>
            <li>Résolution de <br />problèmes complexes</li>
          </ul>
        </div>
        <div class="madskills">
          <ul>
            <li><h3>Loisirs</h3></li>
            <li>Piano</li>
            <li>Violon</li>
            <li>Cuisine</li>
            <li>Jeux vidéos</li>
            <li>Animation et mangas</li>
          </ul>
        </div>
      </div>
      <div class="right-section">
        <div class="experience">
          <ul>
            <li><h3>Expériences professionnelles</h3></li>
            <li>
              <span class="date">2021-2022:</span>
              <p>
                  Stage de 3 mois chez HoudiniEGM pour réaliser leur projet de MOOC en VueJS et Symfony
              </p>
            </li>
            <li>
              <span class="date">2020-2021:</span>
              <p>
                Professeur de mathématiques -
                <a
                  href="https://www.acadomia.fr"
                  title="Plus d'informations sur ACADOMIA"
                  target="_blank"
                  >ACADOMIA</a
                >
                (600+ heures de cours)
              </p>
            </li>
            <li>
              <span class="date">2018-2019:</span>
              <p>
                Professeur de mathématiques - Collège Roger Salengro, HOUPLINES
              </p>
            </li>
          </ul>
        </div>
        <div class="formation">
          <ul>
            <li><h3>Formations/Certifications</h3></li>
            <li>
              <span class="date">2021:</span>
              <p>Formation développeur web chez SIMPLON, Boulogne sur mer</p>
              <p>Titre RNCP de niveau III (BAC+2)</p>
            </li>
            <li>
              <span class="date">2020:</span>
              <p>Master MEEF (Mathématiques) – Lille1, LILLE</p>
            </li>
            <li>
              <span class="date">2019:</span>
              <p>CLES Anglais Niveau2, LILLE</p>
            </li>
            <li>
              <span class="date">2018:</span>
              <p>CAPES externe (Mathématiques)</p>
            </li>
            <li>
              <span class="date">2016-2017:</span>
              <p>Licence de Mathématiques – UFR ST, BESANCON</p>
            </li>
            <li>
              <span class="date">2013-2015:</span>
              <p>
                MPSI/MP (CPGE scientifique) – Lycée Leconte de Lisle, SAINT
                DENIS
              </p>
            </li>
          </ul>
        </div>
      </div>
    </section>

    <footer>
      <div class="left-section">
        <ul>
          <li><h3>Liens:</h3></li>
          <li>
            <a href="https://github.com/LucFERRO" title="" target="_blank"
              >GitHub</a
            >
          </li>
          <li>
            <a
              href="https://www.linkedin.com/in/luc-ferro-086b73205/"
              title="Linkedin Luc FERRO"
              target="_blank"
              >Linkedin</a
            >
          </li>
        </ul>
      </div>
      <div class="right-section">
        <ul>
          <li><h3>Contacts:</h3></li>
          <li>07 83 95 94 63</li>
          <li>luchenri.ferro@gmail.com</li>
        </ul>
        <!-- <button class="b" onclick="Button()">Dark mode<img</button> -->
        <a id="button" title="Trop de lumière?" @click="Button()">
          <img id="ON" src="@/assets/img/ONopti.png" alt="OFF"
        /></a>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "CV",
  methods: {
    /* Dark mode */
    Button() {
      var bulbon = document.getElementById("ON");
      var element = document.getElementsByClassName("right-section");
      for (var right of element) {
        right.classList.toggle("dark-mode");
      }
      var element2 = document.getElementsByClassName("left-section");
      for (var left of element2) {
        left.classList.toggle("dark-mode");
      }

      if (element[0].classList.contains("dark-mode")) {
        bulbon.setAttribute("src", "assets/img/OFFopti.png");
        bulbon.setAttribute("title", "Pas assez de lumière?");
      } else {
        bulbon.setAttribute("src", "assets/img/ONopti.png");
        bulbon.setAttribute("title", "Trop de lumière?");
      }
    },
  },
};
</script>

<style scoped>
</style>
