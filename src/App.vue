<template>
  <div id="app">
    <Repo />
    <Nav />
    <div class="container page-container">
      <div class="vue-countries-cities">
        <div class="live-select">
          <div class="select-text">
            <div>
              Select Country: <span>{{ country }}</span>
            </div>
            <div>
              Select City: <span>{{ city }}</span>
            </div>
          </div>
          <vueCountriesCities
            @country="country = $event"
            @city="city = $event"
          />
        </div>
      </div>
      <Warning />
    </div>
  </div>
</template>

<script>
import Nav from "./components/Nav";
import vueCountriesCities from "vue-countries-cities";
import Repo from "./components/Repo";
import Warning from "./components/Warning.vue";
export default {
  name: "App",
  data() {
    return {
      country: "",
      city: ""
    };
  },
  components: { Nav, vueCountriesCities, Repo, Warning }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Baloo+Tamma+2:wght@400;600&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Baloo Tamma 2", cursive;
}
body {
  background: #fafcfd;
}
a {
  text-decoration: none;
  color: inherit;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
}
.page-container {
  display: flex;
  justify-content: space-evenly;
  flex-direction: column;
  min-height: calc(100vh - 120px);
}
.countries-cities .select-box:first-child {
  margin-right: 30px;
}
.vue-countries-cities {
  min-height: 200px;
  display: grid;
  place-content: center;
  .select-text {
    margin-bottom: 10px;
    font-size: 18px;
    display: flex;
    div {
      flex: 1;
      text-align: left;
      &:last-child {
        padding-left: 30px;
      }
      span {
        display: block;
        color: #ef1716;
        font-size: 20px;
        font-weight: bold;
      }
    }
  }
}

@media (max-width: 1200px) {
  .container {
    max-width: 100%;
    padding: 0 20px;
  }
}
@media (max-width: 680px) {
  .countries-cities {
    flex-direction: column;
    .select-box:first-child {
      margin-right: 0;
      margin-bottom: 30px;
    }
  }
}
</style>
