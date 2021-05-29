<template>
  <v-app>
    <!-- <v-card height="100%" width="256" class="mx-auto">       -->
    <v-navigation-drawer width="255px" permanent>
      <v-list-item>
        <!-- <v-list-item-avatar>
          <v-img src="https://media-exp1.licdn.com/dms/image/C4D03AQFMDK5jwBuaNw/profile-displayphoto-shrink_800_800/0/1558872892586?e=1627516800&v=beta&t=fOGOhBHtwXuNj7CSszsQP_qmCXS4TDKAux5ftrdzU2Q"></v-img>
        </v-list-item-avatar> -->
        <v-list-item-content>
          <v-list-item-title class="title">
            Barnabas Tinarwo
          </v-list-item-title>
          <v-list-item-subtitle>
            Software Developer
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- </v-card> -->
    <v-main>
      <slot />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "About", icon: "mdi-account-box-outline" },
        { title: "Projects", icon: "mdi-apps" },
        { title: "Education", icon: "mdi-school-outline" },
        { title: "Contact", icon: "mdi-message-text-outline" },
      ],
      right: null,
    };
  },
};
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
.v-application--wrap {
  flex-direction: row;
}
.v-main {
  flex: 1 0;
}
</style>
