<script setup>

</script>
<template>
  <div class="flex flex-col h-screen bg-gradient-to-br from-blue-500 to-pink-600">
    <header class="shrink-0 flex justify-between bg-white px-4 py-3">
      <a class="text-3xl font-black tracking-tight text-indigo-600" href="/">Work Management</a>
      <nav>
        <a class="text-sm font-medium px-3 py-2 rounded-md hover:bg-gray-100" href="#">My Boards</a>
        <button class="ml-3">
          <img class="h-10 w-10 inline rounded-full" src="https://i.ibb.co/7G8fhHS/Whats-App-Image-2023-05-06-at-12-27-47-AM-1.jpg" alt="">
        </button>
      </nav>
    </header>

    <main class="flex-1 overflow-hidden">
      <div class="flex flex-col h-full">
        <div class="shrink-0 flex justify-between items-center p-4 b from-purple-700 to-pink-800 rounded-t-lg">
          <h1 class="text-3xl text-white font-bold">Board Title</h1>
          <div>
            <button class="inline-flex items-center bg-white/10 hover:bg-white/20 px-3 py-2 font-medium text-sm text-white rounded-md">
              <DotsHorizontal class="w-6 h-6 text-white" />
              <span class="ml-1 text-white">Settings</span>
            </button>
          </div>
        </div>
        <div class="flex-1 overflow-x-auto">
          <div class="inline-flex h-full items-start px-4 pb-4 space-x-4">
            <div
              v-for="item in Array.from({length:3})"
              class="w-72 bg-gradient-to-r from-black-300 via-red-400 to-pink-300 max-h-full flex flex-col rounded-md">
              <div class="flex items-center justify-between px-3 py-2  bg-opacity-20 backdrop-blur">
                <h3 class="text-sm font-semibold text-white">To Do</h3>
                <button class="hover:bg-gray-300 w-8 h-8 rounded-md grid place-content-center">
                  <DotsHorizontalIcon class="w-5 h-5 text-white"/>
                </button>
              </div>
              <div class="pb-3 flex flex-col overflow-hidden">
                <div class="px-3 flex-1 overflow-y-auto">
                  <ul class="space-y-3">
                    <li
                      v-for="item in Array.from({length: 7})"
                      class="group relative bg-white bg-opacity-70 backdrop-blur p-3 shadow rounded-md border-b border-gray-300 hover:bg-gray-100">
                      <a href="#" class="text-sm">card item</a>
                      <button class="hidden absolute top-1 right-1 w-8 h-8 bg-gray-50 group-hover:grid place-content-center rounded-md text-gray-600 hover:text-black hover:bg-gray-200">
                        <PencilIcon class="w-5 h-5"/>
                      </button>
                    </li>
                    <li class="group relative bg-white bg-opacity-70 backdrop-blur p-3 shadow rounded-md border-b border-gray-300 hover:bg-gray-100">
                      <a href="#" class="text-sm">card item</a>
                      <button class="hidden absolute top-1 right-1 w-8 h-8 bg-gray-50 group-hover:grid place-content-center rounded-md text-gray-600 hover:text-black hover:bg-gray-200">
                        <PencilIcon class="w-5 h-5"/>
                      </button>
                    </li>
                  </ul>
                </div>

                <div class="px-3 mt-3">
                  <button class="flex items-center p-2 text-sm font-medium text-white hover:text-black hover:bg-white/30 w-full rounded-md">
                    <PlusIcon class="h-5 w-5"></PlusIcon>
                    <span class="ml-1">Add card</span>
                  </button>
                </div>
              </div>
            </div>

            <div class="w-72">
              <button class="flex items-center bg-white/10 w-full hover:bg-white/20 text-white p-2 text-sm font-medium rounded-md">
                <PlusIcon class="w-5 h-5"/>
                <span class="ml-1">Add another list</span>
              </button>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>
