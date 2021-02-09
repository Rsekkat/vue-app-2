<template>
  <ul>
    <li>
      <a href="#"
        ><img
          src="../navbar/img/03-icons-dashboard.png"
          srcset="
            ../navbar/img/03-icons-dashboard@2x.png 2x,
            ../navbar/img/03-icons-dashboard@3x.png 3x
          "
          class="-IconsDashboard"
        />Dashboard</a
      >
    </li>
  </ul>
</template>

<script>
export default {
  name: "NavItem",
  props: {
    subtitle: {
      type: String,
    },
    section: {
      type: String,
    },
    href: {
      type: String,
    },
    logo: {
      type: String,
    },
    sectionItems: {
      type: Array,
      requiered: true,
    },
    imageURL: {
      type: String,
    },
  },
};
