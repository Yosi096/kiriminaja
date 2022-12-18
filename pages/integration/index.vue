<template>
    <div>
      <div class="container xl:w-10/12 2xl:w-9/12 mx-auto px-3">
          <div class="grid xl:grid-cols-6 xl:gap-20">
            <div class="xl:order-2 col-span-3">
                <div class="flex xl:mt-10">
                  <img class="w-full" src="../../assets/image/integration-image.svg" alt="">
                </div>
            </div>
            <div class="xl:col-span-3 xl:order-1 mt-10">
                <div class="mb-7">
                    <h1 class="font-display slider-title xl:leading-tight text-3xl xl:text-5xl font-bold mb-5">Partner Ecosystem & Integrations</h1>
                    <p class="text-lg slider-descriptionxl:w-9/12">Kami bermitra dengan banyak ekspedisi terkemuka untuk membantu mengembangkan bisnis Anda lebih cepat, dan lebih kuat dari sebelumnya.</p>
                </div>
                <ul class="grid gap-y-5 mb-10 text-sm xl:w-9/12">
                  <li class="flex space-x-3">
                      <svg aria-hidden="true" class="flex-shrink-0 w-5 h-5 text-purple-600" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Check icon</title><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
                      <span class="text-base font-normal leading-tight text-gray-500">Beragam pilihan expedisi & Layanan</span>
                  </li>
                  <li class="flex space-x-3">
                      <svg aria-hidden="true" class="flex-shrink-0 w-5 h-5 text-purple-600" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Check icon</title><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
                      <span class="text-base font-normal leading-tight text-gray-500">Support Cash On Delivery</span>
                  </li>
                  <li class="flex space-x-3">
                      <svg aria-hidden="true" class="flex-shrink-0 w-5 h-5 text-purple-600" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Check icon</title><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path></svg>
                      <span class="text-base font-normal leading-tight text-gray-500">Dashboard Monitoring</span>
                  </li>
                </ul>
                <div class="xl:flex gap-3 mb-5 xl:mb-7">
                    <button type="button" class="text-white bg-purple-700 hover:bg-purple-800 focus:ring-4 focus:ring-purple-300 font-medium text-sm px-4 lg:px-5 py-2 lg:py-2.5 sm:mr-2 lg:mr-0 w-70 focus:outline-none rounded-full text-sm px-5 py-2.5 text-center inline-flex items-center">
                      Daftar Gratis
                      <svg class="ml-3" style="width:18px;height:18px" viewBox="0 0 24 24">
                          <path fill="currentColor" d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z" />
                      </svg>
                    </button>
                    <div>
                      <button type="button" class="text-black hover:bg-gray-200 font-medium text-sm px-4 lg:px-5 py-2 lg:py-2.5 sm:mr-2 lg:mr-0text-sm px-5 py-2.5 text-center inline-flex items-center focus:outline-none rounded-full">
                        <svg class="mr-3" style="width:24px;height:24px" viewBox="0 0 24 24">
                          <path fill="#000" d="M21,5C19.89,4.65 18.67,4.5 17.5,4.5C15.55,4.5 13.45,4.9 12,6C10.55,4.9 8.45,4.5 6.5,4.5C4.55,4.5 2.45,4.9 1,6V20.65C1,20.9 1.25,21.15 1.5,21.15C1.6,21.15 1.65,21.1 1.75,21.1C3.1,20.45 5.05,20 6.5,20C8.45,20 10.55,20.4 12,21.5C13.35,20.65 15.8,20 17.5,20C19.15,20 20.85,20.3 22.25,21.05C22.35,21.1 22.4,21.1 22.5,21.1C22.75,21.1 23,20.85 23,20.6V6C22.4,5.55 21.75,5.25 21,5M21,18.5C19.9,18.15 18.7,18 17.5,18C15.8,18 13.35,18.65 12,19.5V8C13.35,7.15 15.8,6.5 17.5,6.5C18.7,6.5 19.9,6.65 21,7V18.5Z" />
                        </svg>
                        Dokumentasi
                      </button>
                    </div>
                </div>
            </div>
          </div>
      </div>
    </div>
</template>

<script>
export default {
  head() {
    return {
        title: "Integrasi - KiriminAja"
    };
  },
}
</script>