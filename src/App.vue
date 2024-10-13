<script>
import AppHeader from "./components/AppHeader.vue";
import AboutUs from "./components/AboutUs.vue";
import AppServices from "./components/AppServices.vue";
import AppModel from "./components/AppModel.vue";
import UsContacts from "./components/UsContacts.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  name: "App",
  components: {
    AppHeader,
    AboutUs,
    AppServices,
    UsContacts,
    AppFooter,
    AppModel,
  },
  data() {
    return {};
  },
  methods: {},
  mounted() {},
};
</script>
<template>
  <AppHeader />
  <AboutUs id="aboutus" />
  <AppServices id="services" />
  <AppModel id="model" />
  <UsContacts id="contacts" />
  <AppFooter />
</template>
<style>
#app {
  font-family: "Helvetica", sans-serif;
  width: 100%;
}
* {
  padding: 0px;
  margin: 0px;
  border: none;
  font-weight: 400;
  font-style: normal;
  font-family: "Helvetica", sans-serif;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

body,
#app {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background-color: #1c263f;
}

/* Links */

a,
a:link,
a:visited {
  text-decoration: none;
}

a:hover {
  text-decoration: none;
}

/* Common */

aside,
nav,
footer,
header,
section,
main {
  display: block;
}

ul,
ul li {
  list-style: none;
}

img {
  vertical-align: top;
}

img,
svg {
  max-width: 100%;
  height: auto;
}

address {
  font-style: normal;
}

/* Form */

input,
textarea,
button,
select {
  font-family: inherit;
  font-size: inherit;
  color: inherit;
  background-color: transparent;
}

input::-ms-clear {
  display: none;
}

button,
input[type="submit"] {
  display: inline-block;
  box-shadow: none;
  background-color: transparent;
  background: none;
  cursor: pointer;
}

input:focus,
input:active,
button:focus,
button:active {
  outline: none;
  box-shadow: none;
}

button::-moz-focus-inner {
  padding: 0;
  border: 0;
}

.card {
  transition: all 500ms ease;
  cursor: pointer;
}

@media (max-width: 930px) {
  h1 {
    width: 100%;
    font-size: 36px;
    line-height: 36px;
  }
}
</style>
