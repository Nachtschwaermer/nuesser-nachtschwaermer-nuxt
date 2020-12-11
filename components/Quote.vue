<template>
  <section class='bg-quote-picture bg-cover bg-top my-20 jarallax'>
    <div class='bg-gray-800 text-white text-center bg-opacity-60'>
      <blockquote class='container mx-auto py-36'>
        <p class='text-2xl sm:text-3xl md:text-4xl mb-3 font-slab'>{{ quote.text }}</p>
        <cite class='text-lg italic font-title'>{{ quote.cite }}</cite>
      </blockquote>
    </div>
  </section>
</template>
<script>
export default {
  props: ['quote']
};
</script>
