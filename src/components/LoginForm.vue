<script lang="ts" setup>
import { ref } from "vue";
export interface FormSubmit {
    name: string;
    password: string;
} 
const form = ref<FormSubmit>({
    name: '',
    password: ''
});

</script>
<template>
  <div>
    
    <div class="text-center font-bold text-lg text-indigo-800">Login</div>
    <div class="md:grid md:grid-cols-3 md:gap-6">
      <div class="mt-5 md:mt-0 md:col-span-3">
        <form @submit="$emit('submit', form)" >
          <div class="shadow sm:rounded-md sm:overflow-hidden">
            <div class="px-4 py-5 bg-white space-y-6 sm:p-6">
              <div>
                <label for="username" class="block text-sm font-medium text-gray-700"> Username </label>
                <div class="mt-1">
                  <input v-model="form.name" id="username" name="username" class="p-3 shadow-sm focus:ring-indigo-500 focus:border-indigo-500 mt-1 block w-full sm:text-sm border border-gray-300 rounded-md" placeholder="john_doe" />
                </div>
                <p class="mt-2 text-sm text-gray-500">Fill your username</p>
              </div>
            </div>
            <div class="px-4 py-5 bg-white space-y-6 sm:p-6">
              <div>
                <label for="password" class="block text-sm font-medium text-gray-700"> Password </label>
                <div class="mt-1">
                  <input v-model="form.password" type="password" id="password" name="password" class="p-3 shadow-sm focus:ring-indigo-500 focus:border-indigo-500 mt-1 block w-full sm:text-sm border border-gray-300 rounded-md" placeholder="Enter password" />
                </div>
              </div>
            </div>
            <div class="px-4 py-3 bg-gray-50 text-center sm:px-6 flex justify-center items-center">
              <button  type="submit" class="inline-flex justify-center py-2 px-4 border border-transparent shadow-sm text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">Save</button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>