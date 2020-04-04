<template>
  <header>
    <nav class="flex items-center justify-between flex-wrap">
      <div id="line" class="shadow w-screen"></div>
      <div class="flex items-center flex-shrink-0 text-white mr-6">
        <img id="icon-brave" src="../assets/icon-brave@2x.png" class="mr-2" />
        <router-link
          :to="{ name: 'home' }"
          class="font-semibold text-xl tracking-tight text-gray-600"
          >Brave Exchange</router-link
        >
      </div>
      <div
        class="hidden sm:block w-full block flex-grow lg:flex lg:items-center lg:w-auto"
      >
        <div class="text-sm lg:flex-grow">
          <router-link
            v-for="l in links"
            :key="l.title"
            :to="l.to"
            class="block mt-4 lg:inline-block lg:mt-0 text-gray-600 hover:text-pinkg mr-4"
            >{{ l.title }}</router-link
          >
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
// import PxIcon from '@/components/PxIcon'

export default {
  name: 'PxHeader',
  props: {
    links: {
      type: Array,
      default: () => []
    }
  }

  // components: { PxIcon }
}
</script>

<style>
#line {
  height: 30px;
  width: 100%;
  background-image: linear-gradient(to right, #ff335e, #ff9526);
}
#icon-brave {
  width: 50px;
}
</style>
