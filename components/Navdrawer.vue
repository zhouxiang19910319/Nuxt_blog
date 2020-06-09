<template>
  <v-navigation-drawer app v-model="drawer" width="300">
    <v-list> 
      <v-list-item v-for="item in items" :key="item.title" link>
        <v-list-item-content>
          <v-list-item-title class="title d-flex justify-end">{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>

    <template v-slot:append>
      <div class="pa-2">
        <v-btn block>Login</v-btn>
      </div>
    </template>
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "主页" },
        { title: "佛经原文" },
        { title: "佛经潜释" },
        { title: "读书笔记" },
        { title: "联系方式" }
      ]
    };
  }
};
</script>

