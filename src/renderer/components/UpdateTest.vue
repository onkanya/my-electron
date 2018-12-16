<template>
    <v-container>
      <v-text-field
        v-model="name"
        :counter="30"
        label="Name"
        required
      ></v-text-field>
      <v-btn
        @click="submit"
      >
        submit
      </v-btn>
    </v-container>
</template>

<script>
export default {
  data: () => ({
    name: ''
  }),
  methods: {
    submit () {
      console.log(this.name)
    }
  }
}
</script>
