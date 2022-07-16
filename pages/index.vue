<template>


  <div>

    <section class="hero is-primary">
      
        <div class="hero-body">
          <p class="title">
            Enrique Rodríguez
          </p>
          <p class="subtitle">
            Desarollador web y mobile.
          </p>
        </div>
    </section>

    <section class="section">
      <div class="columns">
        <div class="column">
            <b-collapse 
              class="card" 
              animation="slide" 
              aria-id="contentIdForA11y3"
              open="false">
              <template #trigger="props">
                  <div
                      class="card-header"
                      role="button"
                      aria-controls="contentIdForA11y3"
                      :aria-expanded="props.open">
                      <p class="card-header-title">
                          ¿Quien soy?
                      </p>
                      <a class="card-header-icon">
                          <b-icon
                              :icon="props.open ? 'menu-down' : 'menu-up'">
                          </b-icon>
                      </a>
                  </div>
              </template>

              <div class="card-content">
                  <div class="content">
                      Soy un desarollador especializado en aplicaciones webs y Android.<br><br>
                      Actualmente estudio Ingeniería Informática en la Universidad de Murcia. <br><br>
                      He trabajado en varios proyectos de emprendimiento de base tecnológica.
                  </div>
              </div>
              
          </b-collapse>
        </div>
        <div class="column">
          <b-collapse 
            class="card" 
            animation="slide" 
            aria-id="contentIdForA11y3"
            open="false">
            <template #trigger="props">
                <div
                    class="card-header"
                    role="button"
                    aria-controls="contentIdForA11y3"
                    :aria-expanded="props.open">
                    <p class="card-header-title">
                        ¿Qué tecnologicas conozco?
                    </p>
                    <a class="card-header-icon">
                        <b-icon
                            :icon="props.open ? 'menu-down' : 'menu-up'">
                        </b-icon>
                    </a>
                </div>
            </template>

            <div class="card-content">
                <div class="content">
                    <b-taglist>
                      <b-tag class="is-info" v-for="tech in favouriteTechs" v-bind:key="tech" size="is-medium">{{tech}}</b-tag>
                    </b-taglist>
                </div>
            </div>
            
        </b-collapse>
        </div>
        <div class="column">
          <b-collapse 
            class="card" 
            animation="slide" 
            aria-id="contentIdForA11y3"
            open="false">
            <template #trigger="props">
                <div
                    class="card-header"
                    role="button"
                    aria-controls="contentIdForA11y3"
                    :aria-expanded="props.open">
                    <p class="card-header-title">
                        ¿Qué me interesa?
                    </p>
                    <a class="card-header-icon">
                        <b-icon
                            :icon="props.open ? 'menu-down' : 'menu-up'">
                        </b-icon>
                    </a>
                </div>
            </template>

            <div class="card-content">
                <div class="content">
                    <b-taglist>
                      <b-tag class="is-info" v-for="int in interests" v-bind:key="int" size="is-medium">{{int}}</b-tag>
                    </b-taglist>
                </div>
            </div>
            
        </b-collapse>
        </div>
      </div>
    </section>
  </div>

</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      favouriteTechs: ["Laravel", "PHP", "Kotlin (Android)", "Java", "Javascript", "Vue.js", "Nuxt.js", "API Rest", "PWA"],
      interests: ["Emprendimiento","Startup","Rap", "Digitalización de servicios","Sistemas integrados","Movilidad y transporte público","Sistemas Inteligentes de Transporte","Seguridad informática y pentesting","Programación competitiva","Diseño de Software","Big Data aplicado al deporte", "Competiciones de freestyle","WebScraping"]
    }
  }
}
</script>


<style>
  body{
    position: absolute;
    width: 100%;
    height: 100%;
    background: #17c0eb;
  }
</style>