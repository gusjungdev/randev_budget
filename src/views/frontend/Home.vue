<template>
  <section class="bg-white">
        <div class="container pt-20 mx-auto">
            <div class="grid md:gap-3 md:grid-cols-4 grid-cols-1 gap md:px-10 px-4 md:py-5 pb-3 ">
                <div class="col-span-3 hover:drop-shadow-md">
                        <h1 class="flex justify-center text-2xl md:text-3xl font-medium tracking-wider rounded-2xl text-gray-700 font-mono p-5 bg-[url('@/assets/img/banner.jpg')]">Expense Tracker</h1>
                </div>
                <div class="col-span-1 md:mt-0 mt-3">
                    <div class="flex justify-end grid md:grid-rows-2 grid-cols-1 text-center">
                    <VueDatePicker v-model="date" :start-date="startDate" focus-start-date placeholder="Select Date"/>
                    <span class="mt-2 text-xl text-center rounded-sm border border-gray-300 ">All transactions</span>
                    </div>
                </div>
            </div>
            <div class="px-10 text-lg">
                <span>Always keep track of your income and expenses.</span>
            </div>
            <div class="grid md:grid-cols-3 grid-cols-1 gap-4 px-10 py-3 mb-10">
                    <div class=" text-left">
                        <img src="@/assets/img/graph1.png" class=" w-full xl:h-72 lg:h-56 md:h-40 sm:h-40 rounded-lg border-2 border-gray-100"/>
                        <router-link to="/income">
                            <button class="px-3 text-lg rounded-xl bg-green-500 hover:bg-green-300 mt-2 hover:animate-bounce">More Details</button>
                        </router-link>
                        <span class="ml-2">Income </span>
                        <span class="text-orange-300"> (Waiting for Chart.js)</span>
                    </div>
                    <div class="rounded-lg text-left">
                        <img src="@/assets/img/graph2.png" class=" w-full xl:h-72 lg:h-56 md:h-40 sm:h-40 rounded-lg border-2 border-gray-100"/>
                        <router-link to="/expense">
                            <button class="px-3 text-lg rounded-xl bg-red-500 hover:bg-red-300 mt-2 hover:animate-bounce">More Details</button>
                        </router-link>
                        <span class="ml-2">Expense</span> 
                        <span class="text-orange-300"> (Waiting for Chart.js)</span>             
                    </div>
                    <div class="rounded-lg text-left">
                        <img src="@/assets/img/graph3.png" class="w-full xl:h-72 lg:h-56 md:h-40 sm:h-40 rounded-lg border-2 border-gray-100 "/>
                        <router-link to="/savings">
                        <button class="px-3 text-lg rounded-xl bg-yellow-500 hover:bg-yellow-300 mt-2 hover:animate-bounce">More Details</button>
                        </router-link> 
                        <span class="ml-2">Savings</span>
                        <span class="text-orange-300"> (Waiting for Chart.js)</span>
                    </div>
            </div>
            
        </div>

  </section>
</template>

<script>

    export default {
      name: 'Home',
      data() {
          return {

                date: new Date(),
                startDate: new Date(2020, 1),

                url: import.meta.env.VITE_APP_URL,
                urlapi: import.meta.env.VITE_APP_URL_API,
                title: import.meta.env.VITE_APP_TITLE
          }
      }
  }
</script>

<style lang="css" scoped>

</style>