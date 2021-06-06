<template>
  <Page>
    <ActionBar>
      <StackLayout>
        <Image class="logo" src="~/assets/instagram.png" />
      </StackLayout>
    </ActionBar>
    <ScrollView>
      <StackLayout>
        <Post v-for="(item, index) in posts" :key="index" :Image="item.Image" />
      </StackLayout>
    </ScrollView>
  </Page>
</template>

<script lang="ts">
//@ts-ignore
import Post from "./Post";

export default {
  data() {
    return {
      posts: [
        {
          Image:
            "https://s2.glbimg.com/iDz2P4tP7Pns9fM_9Zi4ebtXuZI=/smart/e.glbimg.com/og/ed/f/original/2020/11/24/veneza-anuncia-taxa-de-entrada-para-turistas-a-partir-de-2022.jpg",
        },
        {
          Image:
            "https://etacanadavisa.com.br/main/wp-content/uploads/2018/05/image3-3-830x552.jpg",
        },
        {
          Image:
            "https://nespy2aub3if2yow3fcm0t5y-wpengine.netdna-ssl.com/files/2013/11/conhe%C3%A7a-londres-635x359.jpg",
        },
        {
          Image:
            "https://coisasdojapao.com/wp-content/uploads/2017/11/templo-japao.jpg",
        },
      ],
    };
  },
  components: {
    Post,
  },
};
</script>

<style scoped>
ActionBar {
  background-color: #f5f5f5;
  color: #ffffff;
}

.logo {
  width: 100;
}

.message {
  vertical-align: center;
  text-align: center;
  font-size: 20;
  color: #333333;
}
</style>
