<template>
  <div class="container-fluid content">
    <p>Prikazano <b>{{ articles.length }}</b>/<b>{{ articles.length }}</b> artikala!</p>
    <div class="row container-s">
      <div
        class="col-lg-4 col-sm-6 d-flex justify-content-center"
        v-for="(item, id) in articles"
        :key="id.id"
      >
        <div class="card" style="width: 18rem">
          <div class="card-img-top img-style">
            <img class="card-img-top" :src="item.img" :alt="`Odeca${id}`">
          </div>
          <div class="card-body">
            <h5 class="card-title">{{ item.name }}</h5>
            <p class="card-text p-img">
              {{ item.description }}
            </p>
            <div class="row">
              <div class="color-box-container d-flex justify-content-center">
                  <p>Dostupne velicine:</p>
                  <div :key="i" v-for="i in item.sizes">
                    <div class="sizes-box">{{ i }}</div>
                  </div>
                </div>
              
            </div>
            <div class="row">
                <div class="color-box-container d-flex justify-content-center">
                  <p>Dostupne boje:</p>
                  <div :key="i" v-for="i in item.colors">
                    <div @click="changeColor(i, item)" :class="i + ' color-box'"></div>
                  </div>
                </div>
            </div>
            
            <a href="#" class="btn btn-primary price"
              >RSD {{ item.price }}</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Content",
  components: {},
  props: {},
  methods: {
    changeColor(color, i){
      i.img = require(`./images/slika${i.id}_${color}.jpg`);
      console.log(color, i.img);
    }
  },
  data() {
    return {
      articles: [ 
        {
          id: 1,
          name: "Lapel Majica",
          price: "254.99",
          description: "Lapel Majica Kratkih Rukava",
          sizes: ["XS", "M", "L", "XXL"],
          colors: ['white', 'red', 'black'],
          img: require("./images/slika1_white.jpg")
        },
        {
          id: 2,
          name: '"EAST MEETS WEST" Majica',
          price: "374.99",
          description: "EMW Majica Kratkih Rukava",
          colors: ['black'],
          sizes: ['XXS', 'XXL', 'XXL'],
          img: require("./images/slika2_black.jpg")
        },

        {
          id: 3,
          name: "Mobil Racing Majica",
          price: "499.99",
          description: "MR Majica Kratkih Rukava",
          colors: ['brown'],
          sizes: [ 'M', 'L', 'XL', 'XXL'],
          img: require("./images/slika3.jpg")
        },
        {
          id: 4,
          name: "HBL 53 Majica",
          price: "250.99",
          description: "HBL Majica Kratkih Rukava",
          colors: ['gray'],
          sizes: ['XXS', 'XS', 'M', 'XXL'],
          img: require("./images/slika4.jpg")
        },
        {
          id: 5,
          name: "Carp Fishing Majica",
          price: "744.99",
          description: "CF Majica Kratkih Rukava",
          colors: ['black', 'green'],
          sizes: ['XS', 'XL', 'XXL', 'XXL'],
          img: require("./images/slika5_black.jpg")
        },
        {
          id: 6,
          name: "Joker Majica",
          price: "1099.99",
          description: "Joker Majica Kratkih Rukava",
          colors: ['black', 'white'],
          sizes: ['XXL', 'XXL'],
          img: require("./images/slika6_black.jpg")
        },
        {
          id: 7,
          name: "Multicam Suskavac",
          price: "4349.99",
          description: "Suskavac Dugih Rukava",
          colors: ['black', 'green'],
          sizes: ['XXS'],
          img: require("./images/slika7_black.jpg")
        },
        {
          id: 8,
          name: "Multicam Military",
          price: "4999.99",
          description: "Camo Dukserica Dugih Rukava",
          colors: ['brown', 'black'],
          sizes: ['M', 'L', 'XXL', 'XXL'],
          img: require("./images/slika8_brown.jpg")
        },
        {
          id: 9,
          name: "Multicam Duks",
          price: "1499.99",
          description: "Duks dugih rukava",
          colors: ['gray', 'blue', 'white'],
          sizes: ['XXS', 'L', 'XL'],
          img: require("./images/slika9_gray.jpg")
        },
      ],
    };
  },
};
</script>

<style scoped>
  .container-s {
    margin-bottom: 50px;
  }
  .card {
    background-color: #ffffff !important;
  }
  .color-box-container {
    overflow: hidden;
  }

  .color-box-container p {
   float: left;
  }

  .sizes-box {
    margin-left: 0.1rem;
    border: 2px solid black;
    float: left;
    cursor: pointer;
    font-weight: 800;
  }

  .sizes-box:hover {
    background-color: rgb(143, 143, 143);
  }

  .color-box {
    padding: 0.8rem;
    margin-left: 0.1rem;
    box-shadow:inset 0px 0px 0px 4px rgb(0, 0, 0);
    float: left;
    cursor: pointer;
  }  

  .red {
    background-color: rgb(228, 24, 24);
  }

  .blue {
    background-color: rgb(47, 47, 204);
  }

  .white {
    background-color: rgb(255, 255, 255);
  }

  .black {
    background-color: rgb(0, 0, 0);
  }

  .green {
    background-color: rgb(17, 80, 17);
  }

  .gray {
    background-color: rgb(61, 61, 61);
  }

  .brown {
    background-color: rgb(37, 27, 27);
  }

  .card-img-top {
    border: none;
    box-shadow: none;
    filter: none;
    height: 50%;
    cursor: pointer;
    transition: 0.5s ease;
  }

  .card-img-top:hover {
    transform: scale(1.1);
  }

  .img-style {
    overflow: hidden;
  }

  .content {
    margin-top: 50px;
    text-align: center;
  }

  .img-style {
    text-align: center;
    outline: none;
  }

  .card {
    margin: 10px 0px auto;
    background: none;
    overflow: hidden;
  }

  .p-img {
    text-align: center;
  }

  .price {
    height: 100%;
    width: 100%;
    font-size: 17px;
    font-weight: 800;
    background-color: rgb(199, 28, 28);
    border-color: rgb(199, 28, 28);
    color: #ffffff;
  }

  .price:hover {
    border-color: rgb(0, 0, 0);
    background-color: rgb(0, 0, 0);
  }
</style>
