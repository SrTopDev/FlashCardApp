<template>
  <div id="app" class="card-overlay">
    <v-app>
      <div
        :class="{
          'sm-main-style': $vuetify.breakpoint.smAndDown,
          'md-main-style': $vuetify.breakpoint.mdAndUp,
        }"
      >
        <router-view />
      </div>
    </v-app>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;500;600;700;800;900&display=swap");

#app {
  font-family: Raleway, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: url("https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1414&q=80")
    no-repeat center center fixed;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}

.v1 {
  border-left: 1px solid grey;
}

.sm-main-style {
  margin: auto;
  width: 95%;
}
.md-main-style {
  margin: auto;
  width: 90%;
}

.footer-md {
  padding: 30px 0px;
}
.footer-md a {
  text-decoration: none;
  color: white !important;
  font-size: 1.1rem;
  font-family: cursive;
  font-weight: 600;
}

.footer-sm {
  padding: 20px 0px;
}
.footer-sm a {
  text-decoration: none;
  color: white !important;
  font-size: 0.8rem;
  font-family: cursive;
  font-weight: 600;
}

.overflow-hidden {
  overflow: hidden;
}

.button {
  border: none;
  color: #FFF;
  background: #42b983;
  appearance: none;
  font: inherit;
  font-size: 1.8rem;
  padding: .5em 1em;
  border-radius: .3em;
  cursor: pointer;
}

.modal {
  position: absolute;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  text-align: center;
  width: 800px;
  height: fit-content;
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.2);
  background: #FFF;
  z-index: 999;
  transform: none;
}
.modal h3 {
  margin: 0 0 1rem;
}

.modal-overlay {
  content: '';
  position: absolute;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 998;
  background: #2c3e50;
  opacity: 0.6;
  cursor: pointer;
}

/* ---------------------------------- */
.fade-enter-active,
.fade-leave-active {
  transition: opacity .4s linear;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.pop-enter-active,
.pop-leave-active {
  transition: transform 0.4s cubic-bezier(0.5, 0, 0.5, 1), opacity 0.4s linear;
}

.pop-enter,
.pop-leave-to {
  opacity: 0;
  transform: scale(0.3) translateY(-50%);
}


</style>
