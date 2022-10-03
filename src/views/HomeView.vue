<template>
  <div>
    <template>
      <div>
        <v-app-bar
          color="transparent"
          absolute
          elevation="0"
          dark
          class="px-12"
        >
          <v-toolbar-title class="logo font-weight-bold text-h5"
            ><span class="yellow--text">Yee</span>Coffee</v-toolbar-title
          >

          <v-spacer></v-spacer>

          <v-btn small text>Menu</v-btn>
          <v-btn small text>Layanan</v-btn>
          <v-btn small text>Berita</v-btn>
          <v-btn small text>Tentang Kami</v-btn>
          <v-btn small text>Kontak</v-btn>

          <v-spacer></v-spacer>
          <v-btn text small>
            <v-icon left> mdi-map-marker </v-icon>
            Temukan Kami
          </v-btn>
        </v-app-bar>
      </div>
    </template>

    <v-carousel hide-delimiters :show-arrows="false" class="hero" height="750">
      <v-carousel-item
        v-for="(item, i) in images"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
        ><v-row class="fill-height" align="center" justify="center">
          <div class="text-center">
            <div class="mb-2">
              <img src="../assets/coffee-hero.png" alt="" />
            </div>
            <div class="font-weight-bold white--text mb-2 title-hero">
              BEST COFFEE FROM INDONESIAN
            </div>
            <div class="opensans white--text mb-6">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Consectetur nec turpis egestas <br />
              mi feugiat. Interdum nunc donec elementum tellus commodo.
            </div>
          </div>
        </v-row></v-carousel-item
      >
    </v-carousel>
    <div class="px-12 mb-0 our-menu">
      <div class="title-content pt-10 text-center">OUR MENU</div>
      <v-row class="mt-0 pt-0">
        <v-col>
          <v-card
            :loading="loading"
            class="mx-auto my-12 text-center"
            max-width="328"
            flat
            color="transparent"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="210"
              src="https://ik.imagekit.io/yudha/YeeCoffee/Coffee-based_drinks_Z4g9T6VqC.png?ik-sdk-version=javascript-1.4.3&updatedAt=1664761602839"
            ></v-img>

            <div class="font-weight-bold menu-title mt-4">
              COFFEE-BASED DRINKS
            </div>
            <div class="opensans menu-subtitle white--text mt-1">
              Dari minunan tradisional berbasis espresso sampai berbagai minuman
              racikan kopi terkini.
            </div>
          </v-card>
        </v-col>
        <v-col>
          <v-card
            :loading="loading"
            class="mx-auto my-12 text-center"
            max-width="328"
            flat
            color="transparent"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="210"
              src="https://ik.imagekit.io/yudha/YeeCoffee/non-coffee_31NA8p5mR.png?ik-sdk-version=javascript-1.4.3&updatedAt=1664761602763"
            ></v-img>

            <div class="font-weight-bold menu-title mt-4">NON-COFFEE</div>
            <div class="opensans menu-subtitle white--text mt-1">
              Kami juga memiliki menu non-coffee untuk kamu dan untuk anak -
              anak.
            </div>
          </v-card>
        </v-col>
        <v-col>
          <v-card
            :loading="loading"
            class="mx-auto my-12 text-center"
            max-width="328"
            flat
            color="transparent"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="210"
              src="https://ik.imagekit.io/yudha/YeeCoffee/food_Ww-bUXwVB.png?ik-sdk-version=javascript-1.4.3&updatedAt=1664761602839"
            ></v-img>

            <div class="font-weight-bold menu-title mt-4">FOOD & SNACK</div>
            <div class="opensans menu-subtitle white--text mt-1">
              Berbagai macam makanan siap menemani secangkir kopimu.
            </div>
          </v-card>
        </v-col>
      </v-row>
    </div>

    <div>
      <v-row>
        <v-col class="about">
          <div class="title-content text-center white--text">TENTANG KAMI</div>
          <div class="logo font-weight-bold white--text text-h4 mt-12">
            <span class="yellow--text">Yee</span>Coffee
          </div>
          <div class="opensans mt-4">
            Dimulai dari satu outlet kecil di depan satu minimarket di kota
            Surabaya, kami berkembang menjadi jaringan kedai kopi nasional
            dengan cabang tersebar di banyak kota di Indonesia.
          </div>
          <div class="opensans mt-1">
            Di tahun 2012, kami adalah pionir dan penggagas dalam gerakan bangga
            terhadap kopi Indonesia dengan kampanye "Yes I Drink Indonesian
            Coffee".
          </div>
          <div class="opensans mt-1">
            Di tahun 2017, kami mendapatkan Penghargaan Indonesia Franchise
            Award dari kementerian Perdagangan sebagai Pemenang Nasional.
            Penghargaan ini serta diserahkan langsung oleh bapak Presiden RI
            Joko Widodo...
          </div>
          <v-btn outlined rounded color="#eead53" class="mt-6">
            Read More
          </v-btn>
        </v-col>
        <v-col class="gallery">
          <div class="title-content text-center white--text">GALLERY</div>
          <div class="mt-12">
            <v-row>
              <v-col v-for="n in 6" :key="n" class="d-flex child-flex" cols="4">
                <v-img
                  :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                  :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                  aspect-ratio="1"
                  class="grey lighten-2"
                >
                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>
                </v-img>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row>
    </div>

    <div class="px-12 mb-0 our-menu">
      <div class="title-content pt-10 text-center">TAKE US WITH YOU</div>
      <v-row class="mt-0 pt-0">
        <v-col>
          <v-card
            :loading="loading"
            class="mx-auto my-12 text-center"
            max-width="328"
            flat
            color="transparent"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img height="210" src="../assets/CATERING.svg"></v-img>

            <div class="font-weight-bold menu-title mt-4">CATERING</div>
            <div class="opensans menu-subtitle white--text mt-1">
              Kamu bisa membawa Coffee Toffee dalam acara kantor atau selebrasi
              pribadi kamu
            </div>
          </v-card>
        </v-col>
        <v-col>
          <v-card
            :loading="loading"
            class="mx-auto my-12 text-center"
            max-width="328"
            flat
            color="transparent"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img height="210" src="../assets/COFFEE PACK.svg"></v-img>

            <div class="font-weight-bold menu-title mt-4">COFFEE PACK</div>
            <div class="opensans menu-subtitle white--text mt-1">
              Dalam kemasan 200gr, kamu bisa menikmati kopi specialty arabika
              Coffee Toffee di rumah.
            </div>
          </v-card>
        </v-col>
        <v-col>
          <v-card
            :loading="loading"
            class="mx-auto my-12 text-center"
            max-width="328"
            flat
            color="transparent"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img height="210" src="../assets/HAMPERS.svg"></v-img>

            <div class="font-weight-bold menu-title mt-4">HAMPERS</div>
            <div class="opensans menu-subtitle white--text mt-1">
              Kirimkan kotak berisi biji kopi dan minuman favorit untuk orang
              spesial kamu.
            </div>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data: () => ({
    images: [
      {
        src: "https://ik.imagekit.io/yudha/YeeCoffee/hero_image_rHsw6EKTd.png?ik-sdk-version=javascript-1.4.3&updatedAt=1664761242878",
      },
    ],
  }),
};
</script>

<style scoped>
.v-application {
  font-family: "Ubuntu", sans-serif !important;
}
.v-application .yellow--text {
  color: #eead53 !important;
  caret-color: #eead53 !important;
}
.title-hero {
  font-size: 1.9rem !important;
  font-weight: 700 !important;
  line-height: 2.5rem;
  letter-spacing: 0.0073529412em !important;
}
.title-content {
  font-weight: 400 !important;
  font-size: 14px;
}
.opensans {
  font-family: "Open Sans", sans-serif !important;
  font-weight: 400 !important;
  font-size: 0.9rem !important;
  color: #ffffffaf !important;
}
.our-menu {
  background-color: #eead53;
}
.menu-title {
  font-size: 20px !important;
  color: #442624;
}
.menu-subtitle {
  font-size: 12px;
}
.about {
  background-color: #502d2d;
  color: #ffffffaf;
  padding-left: 96px;
  padding-right: 96px;
  padding-top: 48px;
  padding-bottom: 48px;
}
.gallery {
  background-color: #442624;
  padding-left: 96px;
  padding-right: 96px;
  padding-top: 48px;
  padding-bottom: 48px;
}
</style>
