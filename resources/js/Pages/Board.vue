<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue';
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
</script>
<template>
<AuthenticatedLayout>
  <div class="flex flex-col h-screen bg-gradient-to-br from-blue-500 to-pink-600">
 
    <main class="flex-1 overflow-hidden">
      <div class="flex flex-col h-full">
        <div class="shrink-0 flex justify-between items-center p-4 b from-purple-700 to-pink-800 rounded-t-lg">
          <h1 class="text-3xl text-white font-bold">Board Title</h1>
          <div>
            <button
              class="inline-flex items-center bg-white/10 hover:bg-white/20 px-3 py-2 font-medium text-sm text-white rounded-md">
              <svg class="w-6 h-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                <path strokeLinecap="round" strokeLinejoin="round"
                  d="M10.5 6h9.75M10.5 6a1.5 1.5 0 11-3 0m3 0a1.5 1.5 0 10-3 0M3.75 6H7.5m3 12h9.75m-9.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-3.75 0H7.5m9-6h3.75m-3.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-9.75 0h9.75" />
              </svg>

              <span class="ml-1 text-white">Settings</span>
            </button>
          </div>
        </div>
        <div class="flex-1 overflow-x-auto">
          <div class="inline-flex h-full items-start px-4 pb-4 space-x-4">
            <div v-for="item in Array.from({ length: 3 })"
              class="w-72 bg-gradient-to-r from-black-300 via-red-400 to-pink-300 max-h-full flex flex-col rounded-md">
              <div class="flex items-center justify-between px-3 py-2  bg-opacity-20 backdrop-blur">
                <h3 class="text-sm font-semibold text-white">To Do</h3>
                <button class="hover:bg-gray-300 w-8 h-8 rounded-md grid place-content-center">

                  <Menu as="div" class="relative z-10">

                    <MenuButton>
                      <svg class="w-6 h-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                        strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
                        <path strokeLinecap="round" strokeLinejoin="round"
                          d="M10.5 6h9.75M10.5 6a1.5 1.5 0 11-3 0m3 0a1.5 1.5 0 10-3 0M3.75 6H7.5m3 12h9.75m-9.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-3.75 0H7.5m9-6h3.75m-3.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-9.75 0h9.75" />
                      </svg>

                    </MenuButton>



                    <transition enter-active-class="transition transform duration-100 ease-out"
                      enter-from-class="opacity-0 scale-90" enter-to-class="opacity-100 scale-100"
                      leave-active-class="transition transform duration-100 ease-in"
                      leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-90">

                      <MenuItems
                        class="origin-top-left mt-2 focus:outline-none absolute left-0 bg-white overflow-hidden rounded-md shadow-lg border w-48">

                        <MenuItem v-slot="{ active }">

                        <a href="#" :class="{ 'bg-gray-100': active }" class="block px-4 py-2 text-sm text-gray-700">Add
                          Card</a>

                        </MenuItem>

                        <MenuItem v-slot="{ active }">

                        <a href="#" :class="{ 'bg-gray-100': active }"
                          class="block px-4 py-2 text-sm text-gray-700">Delete Card</a>

                        </MenuItem>

                      </MenuItems>

                    </transition>

                  </Menu>
                </button>


              </div>
              <div class="pb-3 flex flex-col overflow-hidden">
                <div class="px-3 flex-1 overflow-y-auto">
                  <ul class="space-y-3">
                    <li v-for="item in Array.from({ length: 7 })"
                      class="group relative bg-white bg-opacity-70 backdrop-blur p-3 shadow rounded-md border-b border-gray-300 hover:bg-gray-100">
                      <a href="#" class="text-sm">card item</a>
                      <button
                        class="hidden absolute top-1 right-1 w-8 h-8 bg-gray-50 group-hover:grid place-content-center rounded-md text-gray-600 hover:text-black hover:bg-gray-200">
                        <svg class="w-5 h-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                          className="w-6 h-6">
                          <path
                            d="M21.731 2.269a2.625 2.625 0 00-3.712 0l-1.157 1.157 3.712 3.712 1.157-1.157a2.625 2.625 0 000-3.712zM19.513 8.199l-3.712-3.712-12.15 12.15a5.25 5.25 0 00-1.32 2.214l-.8 2.685a.75.75 0 00.933.933l2.685-.8a5.25 5.25 0 002.214-1.32L19.513 8.2z" />
                        </svg>

                      </button>
                    </li>
                    <li
                      class="group relative bg-white bg-opacity-70 backdrop-blur p-3 shadow rounded-md border-b border-gray-300 hover:bg-gray-100">
                      <a href="#" class="text-sm">card item</a>
                      <button
                        class="hidden absolute top-1 right-1 w-8 h-8 bg-gray-50 group-hover:grid place-content-center rounded-md text-gray-600 hover:text-black hover:bg-gray-200">
                        <svg class="w-5 h-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                          className="w-6 h-6">
                          <path
                            d="M21.731 2.269a2.625 2.625 0 00-3.712 0l-1.157 1.157 3.712 3.712 1.157-1.157a2.625 2.625 0 000-3.712zM19.513 8.199l-3.712-3.712-12.15 12.15a5.25 5.25 0 00-1.32 2.214l-.8 2.685a.75.75 0 00.933.933l2.685-.8a5.25 5.25 0 002.214-1.32L19.513 8.2z" />
                        </svg>

                      </button>
                    </li>
                  </ul>
                </div>

                <div class="px-3 mt-3">
                  <button
                    class="flex items-center p-2 text-sm font-medium text-white hover:text-black hover:bg-white/30 w-full rounded-md">
                    <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                      className="w-6 h-6">
                      <path fillRule="evenodd"
                        d="M12 3.75a.75.75 0 01.75.75v6.75h6.75a.75.75 0 010 1.5h-6.75v6.75a.75.75 0 01-1.5 0v-6.75H4.5a.75.75 0 010-1.5h6.75V4.5a.75.75 0 01.75-.75z"
                        clipRule="evenodd" />
                    </svg>


                    <span class="ml-1">Add card</span>
                  </button>
                </div>
              </div>
            </div>

            <div class="w-72">
              <button
                class="flex items-center bg-white/10 w-full hover:bg-white/20 text-white p-2 text-sm font-medium rounded-md">
                <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                  className="w-6 h-6">
                  <path fillRule="evenodd"
                    d="M12 3.75a.75.75 0 01.75.75v6.75h6.75a.75.75 0 010 1.5h-6.75v6.75a.75.75 0 01-1.5 0v-6.75H4.5a.75.75 0 010-1.5h6.75V4.5a.75.75 0 01.75-.75z"
                    clipRule="evenodd" />
                </svg>


                <span class="ml-1">Add another list</span>
              </button>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</AuthenticatedLayout>
</template>
