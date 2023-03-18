<template>
  <div id="app">
    <div class="global-wrapper">
      <header>
        <!-- Header navigation bar -->
        <div class="head-bar">
          <p><strong class="lighter-clr">adamkeyes</strong></p>
          <nav>
            <ul>
              <li v-for="link in socials" :key="link.name">
                <a href="#" target="_blank">
                  <img :src="link.img" :alt="link.alt" />
                </a>
              </li>
            </ul>
          </nav>
        </div>

        <!-- Header title + text -->
        <div class="head-text">
          <img src="./assets/pattern-rings.svg" alt="decorative rings image" id="rings" />
          <h1>
            Nice to meet you!<br />
            I'm <strong>Adam Keyes.</strong>
          </h1>
          <p>
            Based in the UK, I'm a front-end developer passionate about building accessible web apps
            that users love.
          </p>
          <a href="#" target="_blank" id="contact-me" class="contact">contact me</a>
        </div>

        <!-- Header picture + circle svg -->
        <div class="head-picture">
          <img src="../src/assets/image-profile-desktop.webp" alt="Profile picture of Adam Keyes" />
          <svg xmlns="http://www.w3.org/2000/svg" width="129" height="129">
            <circle
              cx="830.5"
              cy="585.5"
              r="64"
              fill="none"
              stroke="#FFF"
              transform="translate(-766 -521)"
            />
          </svg>
        </div>
      </header>

      <!-- Stacks section -->
      <section class="stacks">
        <div class="stack lighter-clr" v-for="stack in stacks" :key="stack.tech">
          <h3>{{ stack.tech }}</h3>
          <p>{{ stack.year }}</p>
        </div>
        <img src="./assets/pattern-rings.svg" alt="decorative rings image" id="rings-stacks" />
      </section>

      <!-- Projects section -->
      <section class="projects">
        <div class="title-contact">
          <h2>Projects</h2>
          <a href="#" target="_blank" class="contact">contact me</a>
        </div>

        <div class="projects-grid">
          <div class="project" v-for="project in projects" :key="project.title">
            <div class="project-img-view">
              <a href="#">
                <div class="hover-links">
                  <a href="#" target="_blank" class="contact">view project</a>
                  <a href="#" target="_blank" class="contact">view code</a>
                </div>
                <img :src="project.img" alt="project.alt" />
              </a>
            </div>
            <div class="legend-txt">
              <h4>{{ project.title }}</h4>
              <p>
                <span v-for="tech in project.techs" :key="tech">{{ tech }}</span>
              </p>
            </div>
          </div>
        </div>
      </section>
    </div>

    <!-- Contact section -->
    <section class="contact-section">
      <img src="./assets/pattern-rings.svg" alt="decorative rings image" id="rings-contact" />
      <div class="contact-grid">
        <div class="contact-text">
          <h2>Contact</h2>
          <p>
            I would love to hear about your project and how I could help. Please fill in the form,
            and I’ll get back to you as soon as possible.
          </p>
        </div>

        <div class="contact-form">
          <form action="post">
            <div class="form-group">
              <label for="name">name</label>
              <input type="text" name="name" id="name" minlength="3" required />
            </div>
            <div class="form-group">
              <label for="email">email</label>
              <input type="email" name="email" id="email" required />
            </div>
            <div class="form-group">
              <label for="message">message</label>
              <textarea name="message" id="message" cols="30" rows="10" required></textarea>
            </div>
            <div class="form-group">
              <input type="submit" value="send message" />
            </div>
          </form>
        </div>
      </div>

      <!--Footer nav bar-->
      <footer>
        <p><strong class="lighter-clr">adamkeyes</strong></p>
        <nav>
          <ul>
            <li v-for="link in socials" :key="link.name">
              <a href="#" target="_blank">
                <img :src="link.img" :alt="link.alt" />
              </a>
            </li>
          </ul>
        </nav>
      </footer>
    </section>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      socials: [
        {
          name: 'github',
          img: require('@/assets/socials/icon-github.svg'),
          alt: 'link to github',
        },
        {
          name: 'frontendmentor',
          img: require('@/assets/socials/icon-frontend-mentor.svg'),
          alt: 'link to front end mentor',
        },
        {
          name: 'linkedin',
          img: require('@/assets/socials/icon-linkedin.svg'),
          alt: 'link to linkedin',
        },
        {
          name: 'twitter',
          img: require('@/assets/socials/icon-twitter.svg'),
          alt: 'link to twitter',
        },
      ],
      stacks: [
        {
          tech: 'HTML',
          year: '4 Years Experience',
        },
        {
          tech: 'CSS',
          year: '4 Years Experience',
        },
        {
          tech: 'Javascript',
          year: '4 Years Experience',
        },
        {
          tech: 'Accessibility',
          year: '4 Years Experience',
        },
        {
          tech: 'React',
          year: '3 Years Experience',
        },
        {
          tech: 'Sass',
          year: '3 Years Experience',
        },
      ],
      projects: [
        {
          title: 'design portfolio',
          img: require('@/assets/thumbnails/thumbnail-project-1-large.webp'),
          techs: ['html', 'css'],
        },
        {
          title: 'e-learning landing page',
          img: require('@/assets/thumbnails/thumbnail-project-2-large.webp'),
          techs: ['html', 'css'],
        },
        {
          title: 'Todo web app',
          img: require('@/assets/thumbnails/thumbnail-project-3-large.webp'),
          techs: ['html', 'css', 'javascript'],
        },
        {
          title: 'Entertainment web app',
          img: require('@/assets/thumbnails/thumbnail-project-4-large.webp'),
          techs: ['html', 'css', 'javascript'],
        },
        {
          title: 'Memory Game',
          img: require('@/assets/thumbnails/thumbnail-project-5-large.webp'),
          techs: ['html', 'css', 'javascript'],
        },
        {
          title: 'Art gallery showcase',
          img: require('@/assets/thumbnails/thumbnail-project-6-large.webp'),
          techs: ['html', 'css', 'javascript'],
        },
      ],
    };
  },
};
</script>

<style>
@font-face {
  font-family: 'Grotesk';
  src: url(./assets/fonts/SpaceGrotesk-VariableFont_wght.ttf);
  font-weight: 100 900;
}

:root {
  /* Colors */
  --clr-darker: hsl(0, 0%, 8%);
  --clr-dark: hsl(0, 0%, 14%);
  --clr-lighter: hsl(0, 0%, 100%);
  --clr-light: hsl(0, 0%, 85%);
  --clr-green: hsl(153, 71%, 59%);
  --clr-red: #ff6f5b;

  /* Fonts sizes */
  --xl-font-size: 88px;
  --l-font-size: 48px;
  --lm-font-size: 32px;
  --m-font-size: 24px;
  --s-font-size: 18px;

  /* Lines height */
  --xl-line-height: 88px;
  --l-line-height: 56px;
  --m-line-height: 32px;
  --s-line-height: 28px;

  /* Letter spacing */
  --h1-char-spacing: -2.5px;
  --h2-char-spacing: -1.5px;

  /* randoms props */
  --global-padding: 15%;
  --global-padding-tablet: 5%;
  --global-padding-phone: 1rem;
}

* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
  border: none;
  box-sizing: border-box;
  font-family: 'Grotesk', 'sans-serif';
  z-index: 1;
}

img {
  max-width: 100%;
  display: block;
}

.lighter-clr {
  color: var(--clr-lighter);
}

h1,
h2 {
  font-weight: bold;
}

h1,
.title-contact h2 {
  font-size: var(--xl-font-size);
  line-height: var(--xl-line-height);
  letter-spacing: var(--h1-char-spacing);
  color: var(--clr-lighter);
}

@media screen and (max-width: 651px) {
  .title-contact h2 {
    font-size: var(--l-font-size);
  }
}

@media screen and (max-width: 1024px) {
  h1 {
    max-width: 30rem;
  }
}

@media screen and (max-width: 651px) {
  h1 {
    max-width: 100%;
    text-align: center;
    font-size: var(--l-font-size);
  }
}

h2 {
  font-size: var(--l-font-size);
  line-height: var(--l-line-height);
  letter-spacing: var(--h2-char-spacing);
}

h3 {
  font-size: var(--m-font-size);
  line-height: var(--m-line-height);
}

h4 {
  text-transform: uppercase;
  font-size: var(--s-font-size);
  color: var(--clr-lighter);
}

p,
.contact {
  font-size: var(--s-font-size);
  line-height: var(--s-line-height);
  font-weight: normal;
}

#app {
  background-color: var(--clr-darker);
}

.global-wrapper {
  padding: 1rem var(--global-padding) 0;
  overflow: hidden;
}

@media screen and (max-width: 1024px) {
  .global-wrapper {
    padding: 1rem var(--global-padding-tablet) 0;
  }
}

@media screen and (max-width: 651px) {
  .global-wrapper {
    padding: 1rem var(--global-padding-phone);
  }
}

@media screen and (max-width: 651px) {
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.head-bar,
footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

footer {
  padding: 2.5rem 0 0 0;
}

@media screen and (max-width: 651px) {
  .head-bar,
  footer {
    flex-direction: column;
  }

  footer p {
    margin: 0 0 1rem 0;
  }
}

.head-bar p strong,
footer p strong {
  font-size: var(--lm-font-size);
}

@media screen and (max-width: 651px) {
  .head-bar p {
    padding: 1.2rem 0;
  }
}

h1 strong {
  box-shadow: 0 5px var(--clr-green);
}

nav ul {
  display: flex;
}

nav ul li {
  padding: 0.7rem 0.7rem;
}

@media screen and (max-width: 651px) {
  nav ul li {
    padding: 0.7rem 1rem;
  }
}

nav ul li a img:hover {
  transition: 0.3s;
  transform: scale(1.2);
}

.head-text {
  padding: 7rem 0 9rem;
  position: relative;
}

@media screen and (max-width: 1024px) {
  .head-text {
    padding: 5.1rem 0 9rem;
  }
}

@media screen and (max-width: 651px) {
  .head-text {
    width: 100%;
    text-align: center;
    order: 3;
  }
}

#rings {
  position: absolute;
  top: 2.8rem;
  left: -15.7rem;
}

@media screen and (max-width: 1024px) {
  #rings {
    top: 1rem;
  }
}

@media screen and (max-width: 651px) {
  #rings {
    top: -23rem;
  }
}

.head-text p {
  color: var(--clr-light);
  width: 27rem;
  padding: 3.5rem 0 3.5rem 0;
}

@media screen and (max-width: 1024px) {
  .head-text p {
    width: 26rem;
    padding: 3.5rem 0 3rem 0;
  }
}

@media screen and (max-width: 651px) {
  .head-text p {
    width: auto;
    padding: 3.5rem;
  }
}

.contact {
  color: var(--clr-lighter);
  text-transform: uppercase;
  border-bottom: solid 2px var(--clr-green);
  padding: 0 0 0.4rem 0;
  transition: color 0.3s;
}

.contact:hover {
  color: var(--clr-green);
  border: none;
}

.head-picture {
  width: 445px;
  height: 720px;
  position: absolute;
  top: 0;
  right: var(--global-padding);
  z-index: 0;
}

@media screen and (max-width: 1024px) {
  .head-picture {
    right: 0;
  }
}

@media screen and (max-width: 651px) {
  .head-picture {
    max-width: 80%;
    height: auto;
    position: relative;
    inset: unset;
    order: 0;
  }
}

.head-picture svg {
  position: absolute;
  bottom: 70px;
  left: -64.5px;
}

@media screen and (max-width: 1024px) {
  .head-picture svg {
    left: unset;
    right: -64.5px;
  }
}

/* Stacks section */
.stacks {
  border-top: 2px solid var(--clr-light);
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  margin: 5rem 0;
  padding: 4rem 0 0;
  position: relative;
}

@media screen and (max-width: 651px) {
  .stacks {
    display: flex;
    flex-direction: column;
    align-items: center;
    border-bottom: 2px solid var(--clr-light);
  }
}

.stack p {
  color: var(--clr-light);
  padding: 1rem 0 3.5rem;
}

@media screen and (max-width: 651px) {
  .stack {
    text-align: center;
  }
}

.stacks img {
  position: absolute;
  bottom: 0;
  right: -15.7rem;
}

@media screen and (max-width: 651px) {
  .stacks img {
    bottom: -45px;
  }
}

/* Projects section */

.title-contact {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}

@media screen and (max-width: 651px) {
  .title-contact {
    align-items: center;
  }
}

.projects-grid {
  display: grid;
  justify-content: space-between;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-row-gap: 3rem;
  grid-column-gap: 5%;
  margin-top: 5rem;
}

@media screen and (max-width: 1024px) {
  .projects-grid {
    grid-column-gap: 3%;
  }
}

@media screen and (max-width: 651px) {
  .projects-grid {
    grid-template-columns: repeat(1, 1fr);
    grid-template-rows: repeat(auto, 1fr);
    grid-row-gap: 5.5rem;
    padding-bottom: 4rem;
  }
}

.project-img-view {
  position: relative;
}

.project-img-view img:hover {
  opacity: 0.3;
}

.hover-links:hover .img-gallery {
  opacity: 0.3;
}

.hover-links {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 3rem;
}

@media screen and (max-width: 651px) {
  .hover-links {
    top: unset;
    left: unset;
    bottom: -7rem;
    transform: translate(0);
    flex-direction: row;
    width: 100%;
    gap: 2rem;
  }
}

.legend-txt {
  padding: 0.8rem 0 0 0;
}

.legend-txt p span {
  color: var(--clr-light);
  margin: 0 1rem 0 0;
}

/* Contact */
.contact-section {
  margin-top: 7rem;
  background-color: var(--clr-dark);
  padding: 3rem var(--global-padding);
  position: relative;
}

#rings-contact {
  position: absolute;
  bottom: 4rem;
  left: -12rem;
}

.contact-grid {
  border-bottom: 2px solid var(--clr-light);
  display: flex;
  justify-content: space-between;
  padding: 0 0 4rem 0;
  gap: 15%;
}

@media screen and (max-width: 1024px) {
  .contact-grid {
    align-items: center;
    flex-direction: column;
    padding: 0 0 4rem 0;
    gap: 2rem;
  }
}

.contact-text {
  flex: 1;
}

.contact-text h2 {
  color: var(--clr-lighter);
}

.contact-text p {
  font-size: var(--s-font-size);
  color: var(--clr-light);
  max-width: 27rem;
  padding: 1.5rem 0 0 0;
}

@media screen and (max-width: 1024px) {
  .contact-text {
    text-align: center;
  }
}

.contact-form {
  flex: 1;
}

@media screen and (max-width: 1024px) {
  .contact-form {
    width: 80%;
  }
}

@media screen and (max-width: 651px) {
  .contact-form {
    width: 100%;
  }
}

.form-group {
  margin: 0.3rem 0;
}

.form-group:nth-child(4) {
  text-align: end;
  margin: 1rem 0 0 0;
}

.form-group label {
  color: var(--clr-light);
  text-transform: uppercase;
  display: block;
  margin: 1rem 0 0 0;
  width: 100%;
  padding: 0 0 0 1rem;
}

.form-group input,
.form-group textarea {
  all: unset;
  border-bottom: 2px solid var(--clr-light);
  margin-bottom: -1px;
  color: var(--clr-lighter);
  padding: 1rem 0 0 0;
  width: 100%;
}

.form-group textarea {
  height: 4rem;
}

.form-group input[type='submit'] {
  color: var(--clr-lighter);
  text-transform: uppercase;
  border-bottom: solid 2px var(--clr-green);
  padding: 0 0 0.4rem 0;
  transition: color 0.3s;
  width: auto;
  cursor: pointer;
}

.form-group input[type='submit']:hover {
  color: var(--clr-green);
}

.form-group *:focus {
  outline: 3px solid var(--clr-light);
  border-radius: 5px;
}
</style>
