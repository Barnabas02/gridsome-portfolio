<template>
  <section id="projects" class="project-section">
    <v-container>
      <v-row>
        <v-col>
          <h1>Projects</h1>
        </v-col>
      </v-row>
      <v-row class="justify-space-around mb-8 mt-4">
        <v-card
          v-for="project in projects"
          :key="project.name"
          class=""
          max-width="300"
        >
          <v-img
            height="200px"
            :src="project.image"
          />
          <v-card-title>{{project.name}}</v-card-title>  
          

          <v-card-text class="text--primary">
            {{truncate(project.description)}}
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text :href="project.github">
              Github Repo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "Curriculum",
          github: "https://github.com/Barnabas02/gridsome-portfolio",
          description: "Curriculum project for Anderson Adventist High School in Gweru Zimbabwe",
          image: "https://image.slidesharecdn.com/curriculumpower-190904142528/95/curriculum-development-1-638.jpg"
        },
        {
          name: "Hour Tracking app",
          github: "https://github.com/Barnabas02/website",
          description: "Hour Tracking app for my car",
          image: "https://www.fittime.co.za/wp-content/uploads/2021/01/f45-1-100x100.png"
        },
      ],
    };
  },
  methods: {
    truncate(str){
      if (str.length >80){
        return str.slice(0,49) + '...'
      }  
      return str
    }
  }
}
</script>

<style scoped>
.project-section {
  background-color: #51c4d3;
}
.v-image {
  border-bottom: 1px solid;
}
</style>
