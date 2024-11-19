<script setup>
import GoodImg from '@/assets/good.png'
import CloseImg from '@/assets/close.png'
import { ref } from 'vue'

const data = ref([
  { subject: '網頁設計', isGood: true },
  { subject: '程式設計', isGood: true },
  { subject: '管理學', isGood: true },
  { subject: '英文', isGood: true },
  { subject: '國文', isGood: true },
  { subject: '體育', isGood: true },
  { subject: '會計', isGood: false },
  { subject: '計算機概論', isGood: false },
  { subject: '現代商業導論與學習方法', isGood: false },
  { subject: '微積分', isGood: false }
])
</script>

<template>
  <section id="about" class="p-8">
    <h2 class="mb-4 text-3xl font-black">About</h2>
    <article class="flex justify-between">
      <div class="card w-[30%] rounded-lg bg-white p-6 shadow-lg">
        <div class="mb-4 flex items-center">
          <img
            src="https://picsum.photos/id/237/200"
            alt="Avatar"
            class="avatar mr-4 h-24 w-24 rounded-full"
          />
          <div>
            <h3 class="text-xl font-bold">Student Name</h3>
            <p class="text-gray-600">Grade Report</p>
          </div>
        </div>
        <ul class="space-y-2">
          <li
            class="flex items-center rounded px-2 py-1 even:bg-sky-200"
            v-for="d in data"
            :key="d.subject"
          >
            <img :src="d.isGood ? GoodImg : CloseImg" class="h-7" alt="" />
            <span class="ml-2">{{ d.subject }}</span>
          </li>
        </ul>
      </div>
      <div class="h-[600px] w-[65%] rounded-lg bg-white p-6 leading-loose shadow-lg">
        <h3 class="mb-4 text-2xl font-bold">Gallery</h3>
        <div class="grid grid-cols-3 gap-5 overflow-y-scroll h-[500px]">
          <img
            v-for="i in 9"
            :key="i"
            :src="'https://picsum.photos/500?random=' + (i + 4)"
            alt=""
            class="shadow transform transition-transform hover:scale-70 hover:rotate-180"
          />
        </div>
      </div>
    </article>
  </section>
</template>

<style scoped>
.avatar {
  animation: anime1 3s linear infinite;
}
.card:hover .avatar {
  animation-play-state: paused;
}

@keyframes anime1 {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
