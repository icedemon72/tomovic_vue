<template>
  <div id="container-fluid">
    <div id="navbar" class="row-fluid">
      <div id="navbar-links">
        <router-link class="route" to="/">PRODAVNICA</router-link>
        <router-link class="route" to="/about">O NAMA</router-link>
        <router-link class="route" to="/contact">KONTAKT</router-link>
      </div>
      <div id="search">
        <input class="search_input" type="text" placeholder="Pretrazite..." />
        <i class="fa-solid fa-magnifying-glass search_btn"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  components: {},
  props: {},
};
</script>

<style scoped>

a:hover {
  color: white;
}

#navbar {
  display: flex;
  background-color: #131516;
  justify-content: space-between;
  height: 80px;
}

#navbar-links {
  display: flex;
  font-size: 25px;
  margin: 20px;
  font-weight: 800;
}

@media (max-width: 550px) {
  #navbar-links {
    font-size: 22px;
  }
  .route {
    padding-top: 5px;
  }
  .brand {
    margin-top: -5px;
  }
}
.route {
  text-decoration: none;
  margin: 0px 10px;
  color: #ffffff;
  transition: 0.3s ease-in;
}
.route:hover {
  background-color: rgb(199, 28, 28);
}
#search {
  display: flex;
  padding: 19px 0px;
  margin-right: 20px;
}
.search_input {
  border-radius: 5px;
  background: #ffffff;
  color: #000000;
  font-weight: 700;
  padding-left: 10px;
  padding: 20px;
  border: 1px solid;
  border-color: #000000;
}
.search_input:focus {
  background:  rgb(199, 28, 28);
  outline: none;
  color: #ffffff;
}
.search_btn {
  color: #ffffff;
  font-size: 25px;
  margin: 9px 10px;
  cursor: pointer;
}

@media (max-width: 730px) {
  #search {
    display: none;
  }
  #navbar {
    justify-content: center;
  }
}

</style>
