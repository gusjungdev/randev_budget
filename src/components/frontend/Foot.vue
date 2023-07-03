<template>
    <footer class="text-white bg-gray-900">
        <div class="container pt-10 mx-auto h-auto  ">
            <div class="flex flex-wrap px-4">
                <div class="w-full md:p-4 md:w-4/12 text-start mb-4">
                    <!-- <img src="@/assets/img/logo-main.webp" class="w-48 mb-6" alt="smart logo" width="192" height="83"/> -->
                    <div class="text-2xl mb-2 text-gray-500"> Contact via</div>
                    <span>Mobile : +66 93-131-7520 </span>
                    <br>
                    <span>E-mail : marryrcp@gmail.com </span>
                    <!-- <div class="mb-4"> 
                        <a href="#" class="hover:text-indigo-200">+1 234 567-890</a>
                        <br>
                        <a href="#" class="hover:text-indigo-200">hello@demo.com</a>
                    </div> -->
                    <!-- <div class="bg-white">
                        <a href="#facebook" title="facebook" class="mr-2 text-xl hover:text-indigo-200"><i class="far fa-facebook "></i></a>
                        <a href="#twitter" title="twitter" class="mr-2 text-xl hover:text-indigo-200"><i class="fa-twitter-square fab"></i></a>
                        <a href="#linkedin" title="linkedin" class="mr-2 text-xl hover:text-indigo-200"><i class="fa-linkedin fab"></i></a>
                    </div> -->
                </div>
                <div class="w-full md:p-4 md:w-8/12 md:text-end ">
                    <h1 class="mb-4 text-lg font-medium text-gray-500 uppercase">ABOUT</h1>
                    <ul>
                        <li class="mb-2">
                            <router-link to="/" class="text-white hover:text-green-400">
                                Dashboard
                            </router-link>
                        </li>
                        <li class="mb-2">
                            <router-link to="/income" class="text-white hover:text-green-400">
                                Income
                            </router-link>
                        </li>
                        <li class="mb-2">
                            <router-link to="/expense" class="text-white hover:text-green-400">
                                Expense
                            </router-link>
                        </li>
                        <li class="mb-2">
                            <router-link to="/savings" class="text-white hover:text-green-400">
                                Savings
                            </router-link>
                        </li>
                        <li class="mb-2">
                            <router-link to="/contact" class="text-white hover:text-green-400">
                                Contact
                            </router-link>
                        </li>
                    </ul>
                </div>

            </div>
            <div class="p-4 text-center md:pt-20 ">
                <hr class="mb-4 opacity-25">
                <p class="text-sm">Copyright © 2023 Randev (Tailwind CSS)</p>
            </div>
        </div> 
    </footer>
</template>

<script>
    export default {
        name: 'Foot'
    }
</script>

<style lang="css" scoped>

</style>