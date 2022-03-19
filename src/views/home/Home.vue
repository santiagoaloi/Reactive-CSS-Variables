<template>
  <v-container class="d-flex justify-center fill-height">
    <v-row>
      <v-col>
        <v-card
          class="card-1 mx-auto white--text"
          :style="style1"
        >
          <v-card-title>
            Vuetfiy's light  theme primary color  
          </v-card-title>
          <code class="ml-3"> $vuetify.theme.themes.light.primary</code>
        </v-card> 
      </v-col>
      <v-col>
        <v-card
          class="card-2 mx-auto white--text"
          :style="style2"
        >
          <v-card-title>
            Custom reactive css color
          </v-card-title>
          <code class="ml-3"> Use either HEX, RGB, name colors</code>

          <v-container>
            <v-text-field
              v-model="customColor"
              solo
            />
          </v-container>
        </v-card> 
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HomeView',

    data() {
      return {
        customColor: 'teal',
      }
    },
  
    computed: {
      style1() {
        return {
          'height' : '400px',
          'width' : '400px',
          '--primary-color': this.$vuetify.theme.themes.light.primary,
        }
      },
      style2() {
        return {
          'height' : '400px',
          'width' : '400px',
          '--custom-color': this.customColor || 'grey',
        }
      },
   
    },
  }
</script>
<style scoped>
  .card-1 {
  	background:  var(--primary-color);
  }
    .card-2 {
  	background:  var(--custom-color);
  }
  </style>