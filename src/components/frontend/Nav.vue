<template>
    <!-- Header -->
    <header class="fixed w-full bg-white z-10 shadow-md " x-data="{menuOpen: false}">
      
        <nav class="container flex flex-wrap  md:px-4 px-1 justify-items-center mx-auto">
    
            <div class="md:w-1/6 w-1/3 text-start">
              <router-link to="/">
                <img src="@/assets/img/logo_new_full.png" alt="logo" class="md:w-28 w-24 p-3"   />
              </router-link>
            </div>

            <div class="md:w-5/6 w-2/3 text-end">
              <button class="lg:hidden px-4 pt-4 ml-auto border-1 navbar-burger" @click="open_menu_mobile()" >
                  <span class="block w-6 my-1 border-b-2 border-current"></span>
                  <span class="block w-6 my-1 border-b-2 border-current"></span>
                  <span class="block w-6 my-1 border-b-2 border-current"></span>
              </button>

              <div class="hidden  pt-3  ml-auto lg:block lg:w-auto ">
                  
                  <router-link to="/" class="block px-4 py-2 font-medium hover:text-indigo-900 hover:bg-blue-50 lg:inline-block">
                    Dashboard
                  </router-link>
                    
                  <router-link to="/income" class="block px-4 py-2 font-medium hover:text-indigo-900 hover:bg-blue-50 lg:inline-block">
                    Income
                  </router-link>

                  <router-link to="/expense" class="block px-4 py-2 font-medium hover:text-indigo-900 hover:bg-blue-50 lg:inline-block">
                    Expense
                  </router-link>

                  <router-link to="/savings" class="block px-4 py-2 font-medium hover:text-indigo-900 hover:bg-blue-50 lg:inline-block">
                    Savings
                  </router-link>

                  <router-link to="/contact" class="block px-4 py-2 font-medium hover:text-indigo-900 hover:bg-blue-50 lg:inline-block">
                    Contact
                  </router-link>

                  <!-- <router-link to="/register" class="block px-4 py-2 font-medium hover:text-indigo-900 lg:inline-block">
                    สมัครสมาชิก
                  </router-link>

                  <div class="inline-block px-4 py-2">
                    <router-link to="/login" class="inline-block px-6 py-2 text-white bg-indigo-600 border-2 border-indigo-600 rounded-md hover:text-indigo-600 hover:bg-indigo-100">
                      เข้าสู่ระบบ
                    </router-link>
                  </div> -->

              </div>
            </div>
        </nav>

        <!-- Mobile Menu -->
        <!-- <div class="absolute inset-x-0 top-0 hidden p-2 transition origin-top transform md:hidden">
            <div class="overflow-hidden bg-white rounded-lg shadow-md ring-1 ring-black ring-opacity-5">
              <div class="flex items-center justify-between px-5 pt-4">
                <div>
                  <img class="w-auto h-8" src="@/assets/img/logo-main.webp" alt="Achieve your life dream" width="160" height="69">
                </div>
                <div class="-mr-2">
                  <button type="button" class="inline-flex items-center justify-center p-2 text-gray-400 bg-white rounded-md hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-cyan-600">
                    <span class="sr-only">Close menu</span>
                    <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                  </button>
                </div>
              </div>
              <div class="pt-5 pb-6" role="menu" aria-orientation="vertical" aria-labelledby="main-menu">

                <div class="px-2 pt-2 pb-3 space-y-1">
                  <a href="#" class="block px-3 py-2 text-base font-medium text-gray-700 rounded-md hover:text-gray-900 hover:bg-gray-50">หน้าหลัก</a>
      
                  <a href="#" class="block px-3 py-2 text-base font-medium text-gray-700 rounded-md hover:text-gray-900 hover:bg-gray-50">เกี่ยวกับเรา</a>
      
                  <a href="#" class="block px-3 py-2 text-base font-medium text-gray-700 rounded-md hover:text-gray-900 hover:bg-gray-50">ผลงาน</a>
      
                  <a href="#" class="block px-3 py-2 text-base font-medium text-gray-700 rounded-md hover:text-gray-900 hover:bg-gray-50">บริการ</a>
                </div>

              </div>
            </div>
        </div> -->

        <div v-if="show_menu_mobile != 'close'" class="navbar-menu relative z-50" >
          <div class="navbar-backdrop fixed inset-0 bg-gray-800 opacity-25"></div>
          <nav class="fixed top-0 left-0 bottom-0 flex flex-col w-5/6 max-w-sm py-6 px-6 bg-white border-r overflow-y-auto">
            <div class="flex flex-row-reverse items-center mb-0">
              <button class="navbar-close text-end" type="button" @click="close_menu_mobile()">
                <svg class="h-6 w-6 text-gray-400 cursor-pointer hover:text-gray-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
              </button>
            </div>
            <div>
              <ul class="text-dark">
                <li class="mb-1 text-dark">
                  <router-link to="/" @click="close_menu_mobile()" class="block px-4 py-2 font-medium text-gray-400  hover:bg-blue-50 hover:text-blue-600 ">
                    Dashboard
                  </router-link>
                </li>
                <li class="mb-1">
                  <router-link to="/income" @click="close_menu_mobile()" class="block px-4 py-2 font-medium text-gray-400  hover:bg-blue-50 hover:text-blue-600 ">
                    Income
                  </router-link>
                </li>
                <li class="mb-1">
                  <router-link to="/expense" @click="close_menu_mobile()" class="block px-4 py-2 font-medium text-gray-400  hover:bg-blue-50 hover:text-blue-600 ">
                    Expense
                  </router-link>
                </li>
                <li class="mb-1">
                  <router-link to="/savings" @click="close_menu_mobile()" class="block px-4 py-2 font-medium text-gray-400  hover:bg-blue-50 hover:text-blue-600 ">
                    Savings
                  </router-link>
                </li>
                <li class="mb-1">
                  <router-link to="/contact" @click="close_menu_mobile()" class="block px-4 py-2 font-medium text-gray-400  hover:bg-blue-50 hover:text-blue-600 ">
                    Contact
                  </router-link>
                </li>
              </ul>
            </div>
            <div class="mt-auto">
              <p class="my-4 text-xs text-center text-gray-400">
                <span>Copyright © 2023</span>
              </p>
            </div>
          </nav>
        </div>

    </header>
</template>

<script>
    export default {
        name: 'Nav',
        data() {
          return {
            show_menu_mobile: 'close',
          }
        },
        methods: {
            open_menu_mobile() {
              this.show_menu_mobile = 'open';
            },
            close_menu_mobile() {
              this.show_menu_mobile = 'close';
            },
        },
        // computed: {
        //   check_status_menu() {
        //     if(this.show_menu_mobile == 'open'){
        //         alert("5555");
        //     }
        //   }
        // },
        // mounted() {
        //     $('.li_menu_mobile').on('click', (evt) => {
        //       console.log("called")
        //         // const data = $(evt.target).data('logId');
        //         // this.logData(data); 
        //     });
        // },
    }

//     // Burger menus
// document.addEventListener('DOMContentLoaded', function() {
//     // open
//     // console.log("saasdas");
//     const burger = document.querySelectorAll('.navbar-burger');
//     const menu = document.querySelectorAll('.navbar-menu');

//     if (burger.length && menu.length) {
//         for (var i = 0; i < burger.length; i++) {
//             burger[i].addEventListener('click', function() {
//                 for (var j = 0; j < menu.length; j++) {
//                     menu[j].classList.toggle('hidden');
//                 }
//             });
//         }
//     }

//     // close
//     const close = document.querySelectorAll('.navbar-close');
//     const backdrop = document.querySelectorAll('.navbar-backdrop');

//     if (close.length) {
//         for (var i = 0; i < close.length; i++) {
//             close[i].addEventListener('click', function() {
//                 for (var j = 0; j < menu.length; j++) {
//                     menu[j].classList.toggle('hidden');
//                 }
//             });
//         }
//     }

//     if (backdrop.length) {
//         for (var i = 0; i < backdrop.length; i++) {
//             backdrop[i].addEventListener('click', function() {
//                 for (var j = 0; j < menu.length; j++) {
//                     menu[j].classList.toggle('hidden');
//                 }
//             });
//         }
//     }
// });
</script>

<style lang="css">
  .router-link-active, .router-link-exact-active{
    color: purple;
  }
</style>