<template>
  <nav class="bg-gray-800 p-4">
    <div class="container mx-auto flex items-center justify-between">
      <h1 class="text-2xl text-white">My Website</h1>
      <ul class="flex space-x-4">
        <li>
          <a href="#home" class="text-white hover:text-gray-400">Home</a>
        </li>
        <li>
          <a href="#about" class="text-white hover:text-gray-400">About</a>
        </li>
        <li>
          <a href="#contact" class="text-white hover:text-gray-400">Contact</a>
        </li>
        <li class="group relative">
          <a href="#dropbar" class="text-white hover:text-gray-400">Dropbar</a>
          <ul
            class="absolute top-5 hidden w-max space-y-2 bg-gray-700 p-2 text-white group-hover:block"
          >
            <li>
              <a href="#option1" class="block p-2 hover:bg-gray-600">選項 1</a>
            </li>
            <li>
              <a href="#option2" class="block p-2 hover:bg-gray-600">選項 2</a>
            </li>
            <li class="group/li relative">
              <a href="#option3" class="block p-2 hover:bg-gray-600">選項 3</a>
              <ul
                class="hidden group-hover/li:block absolute left-full top-0 w-max space-y-2 bg-gray-700 p-2 text-white"
              >
                <li>
                  <a href="#option3-1" class="block p-2 px-1 text-sm hover:bg-gray-600">選項 3-1</a>
                </li>
                <li>
                  <a href="#option3-2" class="block p-2 px-1 text-sm hover:bg-gray-600">選項 3-2</a>
                </li>
              </ul>
            </li>
          </ul>
        </li>
      </ul>
      <form class="flex">
        <input type="text" name="q" placeholder="Search..." class="rounded-l-md p-2 focus:placeholder:invisible" />
        <button type="submit" class="rounded-r-md bg-sky-500 p-2 text-white">Search</button>
      </form>
    </div>
  </nav>
</template>
