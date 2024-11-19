<template>
  <section id="home" class="min-h-[50vh] p-8">
    <h2 class="mb-4 text-3xl font-black">Home</h2>
    <div class="space-y-5">
      <article class="bg-gray-200 p-4 transition-opacity hover:opacity-50">
        <h3 class="text-xl">Welcome to the Home Page</h3>
        <p>碰到我透明度減50%</p>
      </article>
      <article class="bg-gray-200 p-4 transition-opacity hover:opacity-50">
        <h3 class="text-xl">Latest News</h3>
        <p>不要碰我肩膀</p>
      </article>
      <article class="flex flex-col space-x-5 md:flex-row">
        <div
          class="overflow-hidden bg-green-200 p-4 transition-transform hover:rotate-1 hover:scale-105"
        >
          <img
            src="https://picsum.photos/500?random=1"
            alt="Our Mission"
            class="mb-4 h-48 w-full object-cover"
          />
          <h3 class="text-xl">當Hover時</h3>
          <p>Learn more about our mission and values.</p>
        </div>
        <div
          class="overflow-hidden bg-blue-200 p-4 transition-transform hover:rotate-1 hover:scale-105"
        >
          <img
            src="https://picsum.photos/800?random=2"
            alt="Our Team"
            class="mb-4 h-48 w-full object-cover"
          />
          <h3 class="text-xl">要縮放</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla vero doloremque itaque
            quia dolor sint?
          </p>
        </div>
        <div
          class="overflow-hidden bg-pink-200 p-4 transition-transform hover:rotate-1 hover:scale-105"
        >
          <img
            src="https://picsum.photos/800?random=3"
            alt="Our Team"
            class="mb-4 h-48 w-full object-cover"
          />
          <h3 class="text-xl">要旋轉</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, asperiores.</p>
        </div>
      </article>
    </div>
  </section>
</template>
