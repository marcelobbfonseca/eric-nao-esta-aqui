<template>
  <v-layout column justify-center align-center >
    <v-flex xs12 sm8 md6 >
      <div class="text-center">
        <logo />
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline">
          Eric não está, e agora?
        </v-card-title>
        <v-card-text>
          <p>O eric não está aqui, mas deixa sua pergunta aqui que ele responderá assim que voltar!.</p>
          <v-row class="justify-end align-end">
            <v-col>
              <v-text-field v-model="question" label="qual o problema?"></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="2">
              <v-btn @click="googleForMe">ENVIAR</v-btn>
            </v-col>
          </v-row>
          
          <!-- <p>
            Leia o FAQ do eric! <a
              href="https://vuetifyjs.com"
              target="_blank"
            >
              documentation
            </a>.
          </p> -->
          <p>
           Você sabia que pode me encontrar no slack?<a
              href="https://iabs-brasilia.slack.com"
              target="_blank"
              title="slack"
            >
              Slack
            </a>.
          </p>
          <p>Agradeço a sua colaboração e irei te responder assim que puder.</p>
          <div class="text-xs-right">
            <em><small>&mdash; Não está aqui, Eric</small></em>
          </div>
          <hr class="my-3">
          <br>
        </v-card-text>
        <v-card-actions>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  data(){
    return {
      question:''
    }
  },
  methods: {
    googleForMe(){
      window.location.href = `http://letmegooglethat.com/?q=${this.question}`
    }
  }
}
</script>
