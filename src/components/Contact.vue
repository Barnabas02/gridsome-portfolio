<template>
  <section id="contact" class="contact-section" >
    <v-container>
      <v-row>
        <v-col>
          <h1 class="text-center">Contact Information</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col sm="6" offset-sm="3" class="d-flex justify-space-around">
          <v-icon></v-icon>
          <img
            class="contact-icon"
            src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg"
          />
          <img
            class="contact-icon"
            src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg"
          />
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.contact-section {
  background-color: #126e82;
}
.contact-icon {
    height: 30px;

}
</style>
