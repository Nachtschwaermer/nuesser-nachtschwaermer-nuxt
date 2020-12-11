<script src='../../cdu-neuss-processwire/site/templates/resources/cdu-neuss-tailwind/tailwind.config.js'></script>
<template>
  <div>
    <section class='container mx-auto my-20 px-6 flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-24 items-start'>
      <div class='md:pt-2 md:w-1/4'>
        <h2 class='uppercase text-sm tracking-wide border-b border-green-600 font-title'>Die Nachtschwärmer</h2>
      </div>
      <NuxtContent
        class="prose lg:prose-lg w-full md:w-3/4"
        :document="document"
      />
    </section>
    <Statistics :statistics='document.statistics' />
    <Persons :persons='persons' />
    <Quote :quote='document.quote' />
  </div>
</template>

<script>
import Quote from '~/components/Quote'
import Persons from '~/components/Persons'
import Statistics from '~/components/Statistics'
export default {
  components: { Persons, Quote, Statistics },
  async asyncData({ $content, params }) {
    const document = await $content("home").fetch();
    const persons = await $content("persons", params.slug).sortBy('slug').fetch();

    return { document, persons };
  }
};
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
