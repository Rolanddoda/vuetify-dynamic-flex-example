<template>
  <v-container grid-list-md text-xs-center>

    <v-layout row wrap>

      <v-flex xs6>
        <v-text-field label="Set first v-flex" v-model="xs1" prefix="xs" type="number" min="1" max="12"></v-text-field>
      </v-flex>

      <v-flex xs6>
        <v-text-field label="Set first v-flex" v-model="xs2" prefix="xs" type="number" min="1" max="12"></v-text-field>
      </v-flex>

      <v-flex :[firstSection]="true">
        <v-card dark color="primary">
          <v-card-text class="px-0">{{ firstSection }}</v-card-text>
        </v-card>
      </v-flex>

      <v-flex :[secondSection]="true">
        <v-card dark color="primary">
          <v-card-text class="px-0">12</v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    xs1: 6,
    xs2: 6
  }),
  computed: {
    firstSection () {
      return `xs${this.xs1}`
    },
    secondSection () {
      return `xs${this.xs2}`
    }
  }
};
</script>

