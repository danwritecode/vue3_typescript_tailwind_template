<template>
  <div class="text-4xl font-black p-12">
    {{ name }}
    <div class="mt-10">
      <button @click="changeName()" type="button" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
        Change Name
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup() {

    const name = ref('Foo')
    const age = ref<number | string>(25)

    const changeName = () => {
      name.value = 'Bar'
    }
    
    return {
      name,
      age,
      changeName
    }
  },
})
</script>


<style>

</style>