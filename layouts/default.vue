<template>
  <div>
    <header class='w-full h-screen md:h-screen-2/3 bg-green-600 text-white jarallax'>
      <img src='images/zug.jpg' class='absolute top-0 left-o w-full h-full object-cover object-center opacity-20 jarallax-img'>
      <div class='absolute top-0 left-0 w-full h-full flex flex-col justify-center items-center space-y-6 text-center p-12'>
        <img src='images/logo.svg' width='220' height='220' alt='Logo'>
        <h1 class='text-4xl sm:text-5xl md:text-6xl uppercase font-title font-bold'>{{ heading }}</h1>
        <p class='text-xl sm:text-2xl md:text-3xl font-slab'>Mitglied im Corps der Neusser Schützenlust</p>
        <a :href='$config.facebookUrl' target='_blank'>
          <svg class='w-8 h-8 fill-current opacity-75 hover:opacity-100 transform ease-in-out duration-500' xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
        </a>
      </div>
    </header>
    <Nuxt />
    <footer class='text-sm text-gray-600 my-20 px-12 text-center'>
      &copy;{{ currentDate.getFullYear() }} {{ heading }}<br>
      Made with
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" class='fill-current w-4 h-4 mx-px inline-block'>
        <path fill-rule="evenodd" d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z" clip-rule="evenodd" />
      </svg>
      in Neuss
    </footer>
  </div>
</template>
<script>
import config from '../nuxt.config'

export default {
  data() {
    return {
      heading: config.head.title,
      currentDate: new Date
    }
  }
}
</script>
