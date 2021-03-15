<template>
  <Page>
    <Navbar :subtitle="subtitle">
      <template v-slot:content>
        <NavContent> </NavContent>
      </template>
      <template v-slot:item>
        <NavItem
          v-for="navItem in navItems"
          :key="navItem.id"
          :section="navItem.name"
          :imageURL="navItem.imageURL"
        >
        </NavItem>
      </template>
    </Navbar>
  </Page>
</template>

<script>
import Navbar from "./components/navbar/navbar.vue";
import NavItem from "./components/navItem/navItem.vue";
import NavContent from "./components/navContent/navcontent.vue";
import Page from "./components/page/page.vue";

export default {
  name: "App",
  components: {
    Navbar,
    NavItem,
    NavContent,
    Page,
  },
  data() {
    return {
      data: [],
      subtitle: "NOS SERVICES",
      navItems: [
        { name: "test", href: "" },
        { name: "Support", href: "" },
        { name: "centrex", href: "" },
        { name: "mobile", href: "" },
        { name: "trunk", href: "" },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
