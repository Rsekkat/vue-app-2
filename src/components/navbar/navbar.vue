<template>
  <div class="wrapper text">
    <div class="sidebar" id="mySidebar">
      <img
        src="./img/logo-most.png"
        srcset="./img/logo-most@2x.png 2x, ./img/logo-most@3x.png 3x"
        class="logo-Most"
      />
      <a href="javascript:void(0);" class="icon" v-on:click="myFunction()">
        <i class="fa fa-bars"></i>
      </a>
      <div class="section_dashboard">
        <slot name="content"></slot>
      </div>
      <div class="section_service">
        <h5 class="service">{{ subtitle }}</h5>
        <slot name="item"></slot>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Navbar",
  props: {
    subtitle: {
      type: String,
    },
  },
  methods: {
    myFunction() {
      var x = document.getElementById("mySidebar");
      if (x.className === "sidebar") {
        x.className += " responsive";
      } else {
        x.className = "sidebar";
      }
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300&display=swap");
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css");

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  color: white;
  text-decoration: none;
  list-style: none;
}

.-IconsDashboard {
  width: 15px;
  height: 15px;
  margin: 0 10px -2px 0;
  object-fit: contain;
}

.section_dashboard {
  margin-top: 20%;
}

.text {
  width: 32px;
  height: 13px;
  font-size: 13px;
  font-style: normal;
  font-weight: normal;
  font-stretch: normal;
  line-height: normal;
  color: #fff;
  letter-spacing: normal;
}

.wrapper {
  position: relative;
  display: flex;
}

.fas {
  width: 240px;
  height: 39px;
  opacity: 0.2;
}

.sidebar {
  position: fixed;
  width: 260px;
  height: 100%;
  padding: 30px 10px 16px;
  margin: 0 180px 953px 0;
  background: #000;
}

.wrapper .sidebar h2 {
  padding-left: 5%;
  margin-bottom: 30px;
  text-transform: uppercase;
}

.wrapper .sidebar h5 {
  padding-left: 5%;
  margin-bottom: 10px;
  font-size: 10px;
  color: #797979;
}

.wrapper .sidebar .section_service {
  margin-top: 160%;
}

.wrapper .sidebar ul {
  padding-inline-start: 0 !important;
  margin-top: 5px;
}

.wrapper .sidebar ul li {
  width: 240px;
  padding: 5%;
  border-radius: 4px;
}

.wrapper .sidebar ul li a i {
  margin-right: 5px;
}

.wrapper .sidebar .icon_service {
  color: #2bac76;
}

.wrapper .sidebar ul li:hover {
  background-color: rgba(216, 216, 216, 0.2);
}

.wrapper .sidebar ul li:hover a {
  color: #fff;
}

.sidebar .icon {
  display: none;
}

@media screen and (max-width: 700px) {
  .wrapper .sidebar ul {
    display: none;
  }

  .wrapper .sidebar ul li {
    width: 100%;
    padding: 2%;
  }

  .wrapper .sidebar h5 {
    display: none;
  }

  .wrapper .sidebar .service {
    margin-top: 0%;
  }

  .sidebar a.icon {
    display: block !important;
    float: right;
  }

  .sidebar {
    height: 80px;
    width: 100%;
  }

  .sidebar .section_service {
    margin-top: 50% !important;
  }
}

@media screen and (max-width: 700px) {
  .sidebar.responsive .icon {
    display: none;
    position: relative;
    right: 0;
    top: 0;
  }
  .sidebar.responsive ul {
    display: block !important;
    float: none;
    text-align: left;
  }
  .sidebar.responsive {
    width: 100%;
    height: 100%;
    background-color: #000;
  }

  .sidebar.responsive .section_dashboard {
    margin-top: 15%;
  }

  .sidebar.responsive h5 {
    display: block;
  }
}
@media screen and (max-width: 400px) {
  .sidebar .section_service {
    margin-top: 70% !important;
  }

  .wrapper .sidebar ul li {
    padding: 5%;
  }
}
</style>


