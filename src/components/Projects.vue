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
          name: "ECCi Website",
          github: "https://github.com/Barnabas02/gridsome-portfolio",
          description: "Wordpress site for Exalted Christ Church International. A multiracial, multicultural, cosmopolitan church that centers on Manifesting the Reality of God",
          image: "https://scontent.fdur5-1.fna.fbcdn.net/v/t1.6435-9/50448793_2198237127105062_9161160522198941696_n.jpg?_nc_cat=107&ccb=1-3&_nc_sid=09cbfe&_nc_eui2=AeFQK5y9ZJrU00EAiaYL7gpABBM33Tcc4PIEEzfdNxzg8iPGmgK--gGVcQfI8WW1nfPYnHJI-tFjjWSRijmEkcBl&_nc_ohc=9W1Ai5CkmCUAX-rawUZ&tn=J6iWAyGo4-Etj0tD&_nc_ht=scontent.fdur5-1.fna&oh=9cabdb8bcd1e7d97818ee84863b6eb14&oe=60E04EA0"
        },
        {
          name: "Monster Slayer Game",
          github: "https://github.com/Barnabas02/MonsterSlayerGame",
          description: "A Udemy Project to demonstrate VueJS basic functionality and features",
          image: "https://www.fittime.co.za/wp-content/uploads/2021/01/f45-1-100x100.png"
        },
      ],
    };
  },
  methods: {
    truncate(str){
      if (str.length >100){
        return str.slice(0,99) + '...'
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
