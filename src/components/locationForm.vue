<template>
  <form class="columns-3 px-2 sm:px-4 py-2.5">
    <div class="mb-6">
      <label
        for="startLocation"
        class="block mb-2 text-sm font-medium text-white-900 dark:text-gray-300"
        >De</label
      >
      <input
        type="text"
        id="startLocation"
        class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
        placeholder="Ville, Quartier ou Addresse de Depart..."
        required
      />
      <!-- <div v-if="field1" class="alert alert-info">
        Current Value: {{ field1 }}
      </div> -->

      <!-- <place-autocomplete-field
        v-model="field1"
        placeholder="Enter an an address, zipcode, or location"
        label="Address"
        name="field1"
        api-key="AIzaSyAhSv9zWvisiTXRPRw6K8AE0DCmrRMpQcU"
      ></place-autocomplete-field> -->
    </div>
    <div class="mb-6">
      <label
        for="password"
        class="block mb-2 text-sm font-medium text-white-900 dark:text-gray-300"
        >À</label
      >
      <input
        type="text"
        id="endLocation"
        class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
        placeholder="Ville, Quartier ou Addresse de d'Arrive..."
        required
      />
    </div>
    <div class="mb-6">
      <label
        for="dateTime"
        class="block mb-2 text-sm font-medium text-white-900 dark:text-gray-300"
        >Date / Time</label
      >
      <input
        type="text"
        id="dateTime"
        class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
        required
      />
    </div>
  </form>
</template>
<script>
// import Vue from 'vue';
// import VuePlaceAutocomplete from 'vue-place-autocomplete';

// Vue.use(VuePlaceAutocomplete);
export default {
  name: 'location-form',
  data() {
    return { field1: '' };
  },
};
</script>
