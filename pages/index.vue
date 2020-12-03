<template>
  <div
    class="w-100 bg-background"
    style="
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    "
  >
    <div>
      <b-navbar
        class="bg-background"
        toggleable="lg"
        type="dark"
        variant="info"
      >
        <b-navbar-brand style="margin-left: 10px; cursor: pointer">
          <img src="/sunrise.svg" height="70" width="70" />
        </b-navbar-brand>

        <h1 style="color: #000; cursor: pointer; padding-top: 10px">STAY™</h1>

        <b-collapse class="justify-content-center" is-nav>
          <b-navbar-nav class="ml-auto">
            <h5 class="nav-bar-selection">Products</h5>
            <h5 class="nav-bar-selection">Collections</h5>
            <h5 class="nav-bar-selection">About</h5>
            <h5 class="nav-bar-selection" style="margin-right: 0px">Contact</h5>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <h4 class="right-text">Vind verkooppunt</h4>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <div>
      <b-container class="bv-example-row">
        <b-row>
          <b-col>
            <h1 style="font-size: 70px">
              Make <br />
              staying <br />
              home a <br />
              vacation.
            </h1>

            <h4 class="bottom-text" style="margin-top: 30px">
              View our product
            </h4>
          </b-col>
          <b-col>
            <b-img src="/chair.jpg" height="678" width="678" alt="asda" />
          </b-col>
          <b-col>
            <h6>Outdoor</h6>
            <h6>design</h6>
            <h6>forniture</h6>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component
class HomePage extends Vue {
  data() {
    return {
      message: 'Cachorro late, gato mia',
    };
  }
}

export default HomePage;
</script>

<style>
.nav-bar-selection {
  margin-right: 60px;
  cursor: pointer;
  transition: 0.8s;
}

.nav-bar-selection::after {
  content: '';
  width: 0px;
  height: 1px;
  display: block;
  background: black;
  transition: 300ms;
}

.nav-bar-selection:hover::after {
  width: 100%;
}

.right-text {
  margin-right: 40px;
  border-bottom: 2px solid #000;
  padding-bottom: 8px;
  cursor: pointer;
  transition: 0.5s;
}

.right-text:hover {
  color: grey;
  border-bottom: 2px solid grey;
}

.bottom-text {
  width: 68%;
  border-bottom: 2px solid #000;
  padding-bottom: 8px;
  cursor: pointer;
  transition: 0.5s;
  margin-left: 30px;
}

.bottom-text:hover {
  color: grey;
  border-bottom: 2px solid grey;
}
</style>
