<template>
  <ul class="icon_service">
    <li>
      <a href="#"
        ><img
          src="../navbar/img/03-icons-web.png"
          srcset="
            ../navbar/img/03-icons-web@2x.png 2x,
            ../navbar/img/03-icons-web@3x.png 3x
          "
          class="-Icons-Web"
        />{{ section }}
      </a>
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
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300&display=swap");
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css");

.-Icons-Web {
  width: 15px;
  height: 15px;
  margin: 0 10px -2px 0;
  object-fit: contain;
}
</style>
