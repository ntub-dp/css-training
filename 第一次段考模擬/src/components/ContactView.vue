<script setup>
import { ref } from 'vue'

const submitBtn = ref(null)
const textAry = ['愚昧之人是無法點我的','抓不到抓不到','就不讓你送']
const onMouseMove = () => {
  submitBtn.value.style.position = 'absolute'
  const currentHeight = window.scrollY
  const totalHeight = window.scrollY + window.innerHeight
  const currentWidth = 0
  const totalWidth = window.innerWidth

  const randomHeight = Math.floor(Math.random() * (totalHeight - currentHeight)) + currentHeight
  const randomWidth = Math.floor(Math.random() * (totalWidth - currentWidth)) + currentWidth

  submitBtn.value.style.top = `${randomHeight}px`
  submitBtn.value.style.left = `${randomWidth}px`
  submitBtn.value.textContent = textAry[Math.floor(Math.random() * textAry.length)]
}
const onSubmit = () => {
  alert('啊不就好棒棒')
}
</script>

<template>
  <section id="contact" class="min-h-[50vh] p-8">
    <h2 class="mb-4 text-3xl font-black">
      Contact |
      <span class="text-sm"
        >If you have any questions, just fill in the contact form, and we will answer you
        shortly.</span
      >
    </h2>
    <form @submit.prevent="onSubmit" class="space-y-4">
      <div class="grid grid-cols-1 gap-4 md:grid-cols-3">
        <input
          type="text"
          name="name"
          placeholder="Name"
          class="bg-gray-200 px-3 py-5 text-gray-800 placeholder:font-bold placeholder:text-black"
          required
        />
        <input
          type="email"
          name="email"
          placeholder="Email"
          class="bg-gray-200 px-3 py-5 text-gray-800 placeholder:font-bold placeholder:text-black"
          required
        />
        <select
          name="age"
          class="bg-gray-200 px-3 py-5 text-gray-800 *:font-bold placeholder:font-bold placeholder:text-black"
          required
        >
          <option value="" disabled selected class="font-bold">Age</option>
          <option value="under_18">Under 18</option>
          <option value="18_24">18-24</option>
          <option value="25_34">25-34</option>
          <option value="35_44">35-44</option>
          <option value="45_54">45-54</option>
          <option value="55_64">55-64</option>
          <option value="65_over">65 or over</option>
        </select>
      </div>
      <div>
        <textarea
          name="message"
          placeholder="Your message"
          class="w-full bg-gray-200 px-3 py-5 text-gray-800 placeholder:font-bold placeholder:text-black"
          rows="4"
          required
        ></textarea>
      </div>
      <div>
        <button
          type="submit"
          ref="submitBtn"
          @mousemove="onMouseMove"
          class="bg-sky-500 px-14 py-3 text-white font-bold rounded-md"
        >
          Submit
        </button>
      </div>
    </form>
  </section>
</template>
