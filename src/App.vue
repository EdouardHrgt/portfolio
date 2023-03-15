<template>
  <div id="app">
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
        <h1>
          Nice to meet you!<br />
          I'm <strong>Adam Keyes.</strong>
        </h1>
        <p>
          Based in the UK, I'm a front-end developer passionate about building accessible web apps
          that users love.
        </p>
        <div class="contact-circle">
          <a href="#" target="_blank" id="contact-me">contact me</a>
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
      </div>
      <!-- Header picture -->
      <div class="head-picture">
        <img src="../src/assets/image-profile-desktop.webp" alt="Profile picture of Adam Keyes" />
      </div>
    </header>
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
}

* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
  border: none;
  box-sizing: border-box;
  font-family: 'Grotesk', 'sans-serif';
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

h1 {
  font-size: var(--xl-font-size);
  line-height: var(--xl-line-height);
  letter-spacing: var(--h1-char-spacing);
  color: var(--clr-lighter);
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

p,
#contact-me {
  font-size: var(--s-font-size);
  line-height: var(--s-line-height);
  font-weight: normal;
}

#app {
  background-color: var(--clr-darker);
  padding: 1rem 10% 0;
}

.head-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
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

.head-text {
  border: 2px solid var(--clr-red);
  padding: 7rem 0;
}

.head-text p {
  color: var(--clr-light);
  width: 27rem;
  padding: 3rem 0;
}

.contact-circle {
  border: 2px solid rgb(18, 107, 163);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

#contact-me {
  color: var(--clr-light);
  text-transform: uppercase;
  border-bottom: solid 2px var(--clr-green);
  padding: 0 0 0.4rem 0;
}
</style>
