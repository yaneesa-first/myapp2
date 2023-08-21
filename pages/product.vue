<template>
    <Head>
      <Title>Yaneesa Chaisuwan</Title>
    </Head>
    <div v-if="pending">
      Loading ...
    </div>
    <div v-else>
      <div class="container d-flex justify-content-center">
        <form class="w-50 my-5 ">
          <div class="input-group flex-nowrap w-100">
            <input type="text" class="form-control shadow-none" placeholder="Search" aria-label="Username"
              aria-describedby="addon-wrapping">
            <button type="submit" class="btn btn-success"><i class="bi bi-search"></i></button>
          </div>
  
        </form>
      </div>
      <div class="container">
        <div class="grid mb-5">
          <div class="content" v-for="product in Products" :key="product.id">
            <div class="item w-100 h-100 rounded-1" style="border: 0.1px solid black;">
              <div class="content p-3 " style="height: 90%;">
                <img class="priceimg w-50" :src="product.image">
                <h6 class="text-center mt-3">{{ product.title }}</h6>
                <button type="button" class="btn btn-success mt-5 text-white" @click="togglevisible">{{ isvisible? "ซ่อน" : "ดู" }}รายละเอียด</button>
                <div v-show="isvisible">
                <p style="margin-top: 5px;">size : {{ product.size }}</p>
                <p>general : {{ product.general }}</p>
                <p>price : {{ product.price }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  
  
  
  export default {
    data() {
      return {
        Products: [
          {
            id: "1",
            title: "Hermes Constance 18",
            image: "https://www.vendome.mc/wp-content/uploads/2020/01/Hermes_Constance_18_Mini_Chocolat_Epsom_Gold_Hardware_D.jpg",
            size: "18 cm.",
            general: 'Hermes Constance Bag เป็นอีกหนึ่งกระเป๋าที่ขึ้นชื่อในเรื่องของความหายากลองจากรุ่น Birkin และ kelly เลยทีเดียว กระเป๋ารุ่นนี้ออกแบบในปี ค.ศ.1969',
            price: "284,000 bath"
          },
          {
            id: "2",
            title: "Louis Vuitton Pochette Accessoires",
            image: "https://sparklingbeautybee.files.wordpress.com/2022/02/img_8243.jpg?w=750",
            studios: "Asahi Productio",
            general: 'Ever since their father died, Ichiro Kuga has struggled to support his two younger siblings on nothing but a small inheritance and his passion.',
            price: "1500 bath"
          },
          {
            id: "3",
            title: "Prada Cleo Brushed Leather Mini",
            image: "https://media.karousell.com/media/photos/products/2022/8/23/cleo_brushed_leather_mini_bag_1661262808_59558c7a_progressive",
            studios: "Seven Arcs",
            general: "Nasa Yuzaki is determined to leave his name in the history books. Ranking first in the national mock exam and aiming for a distinguished high school,",
            price: "1500 bath"
          },
          {
            id: "4",
            title: "Dior Bobby East-West",
            image: "https://obs.line-scdn.net/r/ect/ect/image_16741160719778370096c6c3616t110522d7",
            studios: "MAPPA",
            general: "In the wake of Eren Yeager's cataclysmic actions, his friends and former enemies form an alliance against his genocidal rampage.",
            price: "1500 bath"
          },
  
        ],
        isvisible: false,
      }
    },
    methods:{
      togglevisible() {
              this.isvisible = !this.isvisible
          },
    }
  
  };
  </script>
  
  <style scope>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    column-gap: 16px;
    row-gap: 30px;
  }
  
  .item:hover {
    box-shadow: -2px 5px 32px -11px rgba(0, 0, 0, 0.86);
  }
  
  .item {
    transition: 0.2s;
  }
  
  .priceimg {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 50%;
  }
  </style>