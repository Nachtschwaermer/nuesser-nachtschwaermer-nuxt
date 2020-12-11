<template>
  <section class='container mx-auto my-20 px-6 flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-24 items-start'>
    <div class='md:pt-2 md:w-1/4'>
      <h2 class='uppercase font-title text-sm tracking-wide border-b border-green-600'>Die Nachtschwärmer</h2>
    </div>
    <ul class='divide-y divide-gray-200 w-full md:w-3/4'>
      <li
        v-for="person in persons"
        :key="person.id"
        class='py-4 flex flex-col md:flex-row justify-between md:items-center'
      >
        <span class='text-lg'>{{ person.title }}</span>
        <span class='text-sm uppercase font-bold text-gray-400 tracking-wide'>{{ person.rank }}</span>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  props: ['persons']
};
</script>
