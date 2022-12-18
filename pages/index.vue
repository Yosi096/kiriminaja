<template>
  <div>
    <div class="container xl:w-10/12 2xl:w-9/12 mx-auto px-3">
        <div class="grid xl:grid-cols-5 xl:gap-14">
          <div class="xl:order-2 col-span-2">
              <div class="flex xl:mt-10">
                <img class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-70 md:rounded-none md:rounded-l-lg" :src="week.img" alt="">
              </div>
          </div>
          <div class="xl:col-span-3 xl:order-1 mt-10" v-for="(employee, i) in bannerFilter(week.id)" :key="i">
                <div class="mb-7">
                    <h1 class="font-display slider-title xl:leading-tight text-3xl xl:text-5xl font-bold mb-5">{{ week.title }}</h1>
                    <p class="text-lg slider-descriptionxl:w-9/12">{{week.sub}}</p>
                </div>
                <ul class="grid gap-y-5 mb-10 text-sm xl:w-7/12" v-if="employee.length">
                  <li class="flex space-x-3" v-for="empl in employee" :key="empl.id">
                      <svg aria-hidden="true" class="flex-shrink-0 w-5 h-5 text-purple-600" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Check icon</title><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
                      <span class="text-base font-normal leading-tight text-gray-500">{{empl.name}}</span>
                  </li>
                </ul>
                <div class="xl:flex gap-3 mb-5 xl:mb-7">
                    <button type="button" class="text-white bg-purple-700 hover:bg-purple-800 focus:ring-4 focus:ring-purple-300 font-medium rounded-lg text-sm px-4 lg:px-5 py-2 lg:py-2.5 sm:mr-2 lg:mr-0 w-70 focus:outline-none rounded-full text-sm px-5 py-2.5 text-center inline-flex items-center">
                      Daftar Gratis
                      <svg class="ml-3" style="width:18px;height:18px" viewBox="0 0 24 24">
                          <path fill="currentColor" d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z" />
                      </svg>
                    </button>
                    <div>
                      <button type="button" class="text-black hover:bg-gray-100 font-medium rounded-lg text-sm px-4 lg:px-5 py-2 lg:py-2.5 sm:mr-2 lg:mr-0text-sm px-5 py-2.5 text-center inline-flex items-center">
                        <svg class="mr-3" style="width:24px;height:24px" viewBox="0 0 24 24">
                          <path fill="#000" d="M21,5C19.89,4.65 18.67,4.5 17.5,4.5C15.55,4.5 13.45,4.9 12,6C10.55,4.9 8.45,4.5 6.5,4.5C4.55,4.5 2.45,4.9 1,6V20.65C1,20.9 1.25,21.15 1.5,21.15C1.6,21.15 1.65,21.1 1.75,21.1C3.1,20.45 5.05,20 6.5,20C8.45,20 10.55,20.4 12,21.5C13.35,20.65 15.8,20 17.5,20C19.15,20 20.85,20.3 22.25,21.05C22.35,21.1 22.4,21.1 22.5,21.1C22.75,21.1 23,20.85 23,20.6V6C22.4,5.55 21.75,5.25 21,5M21,18.5C19.9,18.15 18.7,18 17.5,18C15.8,18 13.35,18.65 12,19.5V8C13.35,7.15 15.8,6.5 17.5,6.5C18.7,6.5 19.9,6.65 21,7V18.5Z" />
                        </svg>
                        Selengkapnya
                      </button>
                    </div>
                </div>
                <div class="flex gap-5">
                    <button type="button" @click="selectemployee(-1)" aria-label="Previous Slider" class="aspect-square prev-slider border p-1 rounded-full hover:bg-purple-200">
                      <svg style="width:24px;height:24px" viewBox="0 0 24 24">
                        <path fill="currentColor" d="M20,11V13H8L13.5,18.5L12.08,19.92L4.16,12L12.08,4.08L13.5,5.5L8,11H20Z" />
                      </svg>
                    </button>
  
                    <div class="flex text-lg font-medium place-items-center gap-3"><span class="text-purple-600">{{week.id +1}}</span><span>/</span><span>{{banner.length}}</span></div>
                    
                    <button type="button" @click="selectemployee(1)" aria-label="Next Slider" class="aspect-square next-slider border p-1 rounded-full hover:bg-purple-200">
                      <svg style="width:24px;height:24px" viewBox="0 0 24 24">
                        <path fill="currentColor" d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z" />
                      </svg>
                    </button>
                </div>
          </div>
        </div>

        <div class="border-gray-100 border-t-2 border-b-2 mt-10">
          <no-ssr>
              <carousel :items="6" :autoplay="true" :nav="false" :dots="false" :loop="true" class="mt-7 mb-7">
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/jne.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/jnt.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/sicepat.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/sap.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/ncs.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/sentral.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/anteraja.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/ninja.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/idx.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/gosend.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/grab_express.png"/>
                  <img class="px-5 py-2 mx-auto lg:pt-2 lg:px-7 flex-1 gap-6" src="../assets/image/ekspedisi/borzo.png"/>
              </carousel>
          </no-ssr>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  props: {
    banner: {
      type:Array,
      default: () => [
        { 
          "data": [
            {"id": "12", "name": "23 Desember 2022"}, 
            {"id": "13", "name": "Pengundian mobil Toyota Calya dan hadiah menarik lainnya"},
            {"id": "14", "name": "Live stream di YouTube dan Instagram KiriminAja"},
          ]
        }, 
        {
          "data": [
            {"id": "22", "name": "Pengiriman Instant"}, 
            {"id": "23", "name": "Mulai dari Rp 2.000/km"},
            {"id": "24", "name": "Bisa diakses di seluruh wilayah Pulau Jawa, Bali, Balikpapan, Banda Aceh, dan Bandar Lampung."},
          ]
        }, 
        {
          "data": [
            {"id": "32", "name": "Ninja Xpress Standard"}, 
            {"id": "33", "name": "Support Penuh dari Ninja"},
            {"id": "34", "name": "Bisa Cash on Delivery"},
          ]
        }, 
        {
          "data": [
            {"id": "42", "name": "Tanpa Biaya Pendaftaran"}, 
            {"id": "43", "name": "Bebas Pilih Ekspedisi"},
            {"id": "44", "name": "Banyak Hadiahnya"},
          ]
        }
      ]
    }
  },
  data() {
    return {
      week: {
        id: 0, 
        title: "Persiapkan Dirimu untuk Pengundian Grand Prize Pestapora 2022", 
        sub: "Catat tanggal dan nyalakan notifikasi di seluruh sosial media KiriminAja biar nggak kelewatan LIVE Streaming Grand Prize Pestapora 2022!",
        img: "https://storage.googleapis.com/tprt0ezsggqjornc7nf1wwluvgulhr/kiriminaja-slider-content/odw89akaPYoL5w5g.webp"
      },
    }
  },
  methods: {
    bannerFilter(w) {
      return this.banner[w]
    },
    selectemployee(w) {
      this.week.id += w;

      if (this.week.id === 1) {
        this.week.id = 1;
        this.week.title = "Borzo Delivery Kini Sudah Hadir di KiriminAja!";
        this.week.sub = "Kini pengiriman instant di KiriminAja makin banyak pilihannya! Update aplikasi KiriminAja-mu dan cobain kirim paket instant pakai Borzo Delivery!";
        this.week.img = "https://storage.googleapis.com/tprt0ezsggqjornc7nf1wwluvgulhr/kiriminaja-slider-content/djDmpUvwP8WgLcjs.webp"
      } else if (this.week.id === 2) {
        this.week.id = 2;
        this.week.title = "Ninja Xpress telah hadir di aplikasi KiriminAja.";
        this.week.sub = "SahabatKA, ada yang baru nih di KiriminAja! Mulai hari ini layanan pengiriman paket Ninja Xpress hadir di aplikasi KiriminAja.";
        this.week.img = "https://kiriminaja.com/storage/Slider/November22/1669273853_Slider (2).png"
      }else if (this.week.id === 3) {
        this.week.id = 3;
        this.week.title = "Gebyar Pesta Pora KiriminAja, Kirim Dapet Cuan";
        this.week.sub = "Cara cerdas KIRIM PAKET pakai KiriminAja banyak diskon dan dapatkan peluang bawa pulang hadiahnya. Yuk buruan daftar dan kirim paketmu sekarang!";
        this.week.img = "https://kiriminaja.com/storage/Slider/April22/1648798905_Slider2 (3) (1).png"
      }else if(this.week.id === -1){
        this.week.id = 3;
        this.week.title = "Gebyar Pesta Pora KiriminAja, Kirim Dapet Cuan";
        this.week.sub = "Cara cerdas KIRIM PAKET pakai KiriminAja banyak diskon dan dapatkan peluang bawa pulang hadiahnya. Yuk buruan daftar dan kirim paketmu sekarang!";
        this.week.img = "https://kiriminaja.com/storage/Slider/April22/1648798905_Slider2 (3) (1).png"
      }else{
        this.week.id = 0;
        this.week.title = "Persiapkan Dirimu untuk Pengundian Grand Prize Pestapora 2022"; 
        this.week.sub = "Catat tanggal dan nyalakan notifikasi di seluruh sosial media KiriminAja biar nggak kelewatan LIVE Streaming Grand Prize Pestapora 2022!";
        this.week.img = "https://storage.googleapis.com/tprt0ezsggqjornc7nf1wwluvgulhr/kiriminaja-slider-content/odw89akaPYoL5w5g.webp";
      }
    }
  }
}
</script>