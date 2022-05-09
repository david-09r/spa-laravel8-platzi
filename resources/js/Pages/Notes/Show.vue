<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';

</script>

<template>
  <AppLayout title="Dashboard">
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">
        Modulo de Notas
      </h2>
    </template>

    <div class="py-12">
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
        <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
          <div class="md:grid md:grid-cols-3 md:gap-6">
            <div class="md:col-span-1">
              <div class="p-0 block sm:flex sm:p-4 sm:flex-col sm:justify-between sm:h-full sm:w-full">
                <div>
                  <h3 class="text-lg text-gray-900">Notas</h3>
                  <p class="text-sm text-gray-600">{{ note.excerpt }}</p>
                </div>
                <Link class="hover:text-green-500" :href="route('notes.index')">Volver</Link>
              </div>
            </div>
            <div class="md:col-span-2 mt-5 md:mt-0">
              <div class="shadow bg-white md:rounded-md p-4">
                <p>{{ note.content }}</p>
                <hr>

              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </AppLayout>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";

export default {
  components: {
    Link,
  },

  props: {
    note: Object
  }
}
</script>