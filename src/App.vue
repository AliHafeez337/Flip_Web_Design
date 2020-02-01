<template>
  <div id="app">
    <div class="container-fluid">
        <div class="row">
            <div class="col-xs-12 col-sm-10 col-sm-offset-1 col-md-10 col-md-offset-1">
                <button class="btn btn-primary" @click="selectedComponent = 'home'">Home</button>
                <button class="btn btn-primary" @click="selectedComponent = 'services'">Services</button>
                <button class="btn btn-primary" @click="selectedComponent = 'aboutus'">About us</button>
                
                <br><br>
                <transition
                        enter-active-class="animated flipInX"
                        leave-active-class="animated flipOutX"
                        mode="out-in"
                >
                    <component :is="selectedComponent"></component>
                </transition>

                <!-- <hr>
                <button class="btn btn-primary" @click="changeNav(1)">Home</button>
                <button class="btn btn-primary" @click="changeNav(2)">Services</button>
                <button class="btn btn-primary" @click="changeNav(3)">About us</button>
                 -->
                <!-- <br />
                <br />
                <div class="flip-card">
                  <div class="flip-card-inner">
                      <div class="flip-card-front">
                          <div class="alert alert-info" key="info">This is some Info</div>
                      </div>
                      <div class="flip-card-back">
                          <div class="alert alert-warning" key="warning">This is some warning</div>
                      </div>
                  </div>
                </div> -->

            </div>
        </div>
    </div>
  </div>
</template>

<script>
    import Home from './Home.vue';
    import Services from './Services.vue';
    import Aboutus from './AboutUs.vue';

export default {
  name: 'app',
  data () {
    return {
      show: false,
      elementWidth: 100,
      selectedComponent: 'home',
      selectedItem: 1,
      from: 1,
      steps: 0
    }
  },
  methods: {
      changeNav(to){
        this.steps = to - this.from
        this.from = to
      }
  },
  components: {
      home: Home,
      services: Services,
      aboutus: Aboutus
  }
  }
</script>

<style>
    #app {
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
    }
</style>
