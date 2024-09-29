<template >
  <section class="text-white mt-18" id="about">
      <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
          <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"></div>
      </div>
      <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
          <div data-aos="flip-right">
              <h2 class="text-4xl font-bold text-white text-left mb-8">My Education</h2>
              <div class="space-y-8 py-8">
                  <div v-for="element in education" :key="element.id"
                  class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
                  >
                      <div class="w-1/4">
                          <img src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation-cap--v1">
                      </div>
                      <div class="w-3/4 pl-4">
                          <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                              {{ element.School }}
                          </h3>
                          <p class="text-white">{{ element.program }}</p>
                          <p class="text-white">{{ element.year }}</p>
                      </div>
                  </div>
              </div>
          </div>
          <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
              <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">More
                  <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">About</span>
                  Me
              </h2>
              <p class="text-base lg:text-lg mt-8 py-8">
              My name is Govind, and I’m currently pursuing a BSc in Computer Science at
              Savitribai Phule Pune University. During my studies, I developed a strong interest in
              backend development, particularly using Python and Django. 
              Over the past few months, I’ve been honing my skills in this area by working on several projects, 
              including an E-commerce API using Django Rest Framework and PostgreSQL, and a cloud-based task automation system named 'Cloud Crusader.'
              <br>
              In my spare time, I enjoy exploring new technologies, staying updated on the latest 
              trends in web development, and contributing to open-source projects. I’m confident that 
              my strong foundation in Python and Django, combined with my proactive approach to learning and
              problem-solving, makes me a great fit for the software developer role.
      </p>
              
          </div>
      </div>
  </section>
</template>
<script setup>
import { ref } from 'vue';
const education=ref([
{
  id: 1,
  School: 'Pune University',
  program: " Bsc Computer Science",
  year: '2025'
}
  
])
</script>
