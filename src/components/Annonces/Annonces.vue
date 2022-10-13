<template>
  <div
    class="grid grid-cols-4 gap-4 place-content-stretch h-48 px-2 sm:px-4 py-2.5"
  >
    <div v-for="(user, index) in users" :key="index">
      <div
        class="w-full max-w-sm bg-white rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700"
      >
        <div class="flex justify-end px-4 pt-4">
          <button
            id="dropdownButton"
            data-dropdown-toggle="dropdown"
            class="inline-block text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 focus:ring-4 focus:outline-none focus:ring-gray-200 dark:focus:ring-gray-700 rounded-lg text-sm p-1.5"
            type="button"
          >
            <span class="sr-only">Open dropdown</span>
            <svg
              class="w-6 h-6"
              aria-hidden="true"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M6 10a2 2 0 11-4 0 2 2 0 014 0zM12 10a2 2 0 11-4 0 2 2 0 014 0zM16 12a2 2 0 100-4 2 2 0 000 4z"
              ></path>
            </svg>
          </button>
          <!-- Dropdown menu -->
          <div
            id="dropdown"
            class="hidden z-10 w-44 text-base list-none bg-white rounded divide-y divide-gray-100 shadow dark:bg-gray-700"
          >
            <ul class="py-1" aria-labelledby="dropdownButton">
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                  >Edit</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 text-sm text-gray-700 hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                  >Export Data</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 text-sm text-red-600 hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                  >Delete</a
                >
              </li>
            </ul>
          </div>
        </div>
        <div class="flex flex-col items-center pb-10">
          <img
            :src="user.img"
            class="mb-3 w-24 h-24 rounded-full shadow-lg"
            alt="Random User Pic"
          />

          <h5 class="mb-1 text-xl font-medium text-gray-900 dark:text-white">
            {{ user.name }}
          </h5>
          <span class="text-sm text-gray-500 dark:text-gray-400">{{
            user.jobTitle
          }}</span>
          <h5
            class="mb-1 text-xl font-medium text-gray-900 dark:text-white"
            style="display: contents"
          >
            {{ user.startTrip }}

            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 384 512"
              style="max-height: 0.7rem; display: inline"
            >
              <!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
              <path
                d="M169.4 470.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 370.8 224 64c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 306.7L54.6 265.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"
              />
            </svg>
            {{ user.endTrip }}
          </h5>
          <div class="flex mt-4 space-x-3 md:mt-6">
            <a
              href="#"
              class="inline-flex items-center py-2 px-4 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
              >Réserver</a
            >
            <a
              href="#"
              class="inline-flex items-center py-2 px-4 text-sm font-medium text-center text-gray-900 bg-white rounded-lg border border-gray-300 hover:bg-gray-100 focus:ring-4 focus:outline-none focus:ring-gray-200 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-700 dark:focus:ring-gray-700"
              >Message</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { faker } from '@faker-js/faker';
import axios from 'axios';

export default {
  name: 'annonces',
  data() {
    return {
      users: [],
    };
  },
  created() {
    for (let index = 0; index < 6; index++) {
      this.users.push({
        name: faker.name.fullName(),
        img: faker.image.avatar(),
        jobTitle: faker.name.jobTitle(),
        startTrip: faker.address.city(),
        endTrip: faker.address.city(),
      });
    }
  },
  methods: {},
};
</script>
