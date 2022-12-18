<template>
    <header class="">
        <nav class="bg-white px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 left-0 border-b border-gray-200">
            <div class="container flex flex-wrap items-center justify-between mx-auto">
                <a href="/" class="flex items-center">
                    <img src="../../assets/image/logo.png" class="h-6 mr-3 sm:h-9" alt="Logo" />
                </a>
                <div class="flex items-center lg:order-5 ">
                    <li>
                        <div class="block py-2 pl-3 pr-4 text-gray-700 border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-purple-700 lg:p-0  mr-5">Masuk</div>
                    </li>
                    <button type="button" class="text-white bg-purple-700 hover:bg-purple-800 focus:ring-4 focus:ring-purple-300 font-medium rounded-lg text-sm px-4 lg:px-5 py-2 lg:py-2.5 sm:mr-2 lg:mr-0 w-70 focus:outline-none rounded-full text-sm px-5 py-2.5 text-center inline-flex items-center">
                        Daftar Gratis
                        <svg class="ml-3" style="width:18px;height:18px" viewBox="0 0 24 24">
                            <path fill="currentColor" d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z" />
                        </svg>
                    </button>
                </div>
                <div class="items-center justify-between hidden w-full lg:flex lg:w-auto lg:order-1" id="mobile-menu-2">
                    <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
                        <li>
                            <div class="block py-2 pl-3 pr-4 text-gray-700 border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-purple-700 lg:p-0 ">Blog</div>
                        </li>
                        <li>
                            <div class="block py-2 pl-3 pr-4 text-gray-700 border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-purple-700 lg:p-0 ">Kabar</div>
                        </li>
                        <li>
                            <button id="dropdownNavbarLink" data-dropdown-toggle="dropdownNavbar" class="flex items-center justify-between w-full py-2 pl-3 pr-4 font-medium text-gray-700 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 md:w-auto">Layanan <svg class="w-5 h-5 ml-1" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg></button>
                            <div id="dropdownNavbar" class="z-10 hidden font-normal bg-white divide-y divide-gray-100 rounded-3xl shadow-2xl w-80 border-1">
                                <div class="flex gap-4 place-items-center border border-transparent hover:border-purple-300 p-3 hover:bg-purple-50 rounded-2xl">
                                    <div class="top-0 left-0 w-full h-full absolute"></div>
                                    <div>
                                        <div class="p-4 rounded-full bg-gradient-to-br from-purple-200">
                                            <svg xmlns="http://www.w3.org/2000/svg" class="brand-google-analytics" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                                <rect x="10" y="9" width="4" height="12" rx="1.105"></rect>
                                                <rect x="17" y="3" width="4" height="18" rx="1.105"></rect>
                                                <circle cx="5" cy="19" r="2"></circle>
                                            </svg>
                                        </div>
                                    </div>
                                    <div>
                                        <h6 class="font-medium">Manajemen Order</h6>
                                        <p class="text-sm text-neutral-500">Platform management order dengan multi ekspedisi</p>
                                    </div>
                                </div>
                                <div class="flex gap-4 place-items-center border border-transparent hover:border-purple-300 p-3 hover:bg-purple-50 rounded-2xl">
                                    <div class="top-0 left-0 w-full h-full absolute"></div>
                                    <div>
                                        <div class="p-4 rounded-full bg-gradient-to-br from-purple-200">
                                            <svg xmlns="http://www.w3.org/2000/svg" class="git-branch" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                                <circle cx="7" cy="18" r="2"></circle>
                                                <circle cx="7" cy="6" r="2"></circle>
                                                <circle cx="17" cy="6" r="2"></circle>
                                                <line x1="7" y1="8" x2="7" y2="16"></line>
                                                <path d="M9 18h6a2 2 0 0 0 2 -2v-5"></path>
                                                <polyline points="14 14 17 11 20 14"></polyline>
                                            </svg>
                                        </div>
                                    </div>
                                    <div>
                                        <h6 class="font-medium">Integrasi API</h6>
                                        <p class="text-sm text-neutral-500">Hubungkan bisnis online existingmu dengan kami</p>
                                    </div>
                                </div>
                            </div>
                        </li>
                        <li>
                            <div class="block py-2 pl-3 pr-4 text-gray-700 border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-purple-700 lg:p-0 ">Cek Ongkir</div>
                        </li>
                        <li>
                            <div class="block py-2 pl-3 pr-4 text-gray-700 border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-purple-700 lg:p-0 ">Lacak</div>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>