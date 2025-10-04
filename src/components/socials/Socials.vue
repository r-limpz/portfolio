<template>
  <div class="flex space-x-4">
    <a
      v-for="link in links"
      :key="link.name"
      :href="link.url"
      target="_blank"
      rel="noopener noreferrer"
      class="w-[35px] h-[35px] bg-gray-950/60 p-2 border rounded-full border-cyan-300 flex items-center text-center space-x-2 text-cyan-300 hover:text-gray-800 hover:bg-cyan-300 transition-colors duration-300"
    >
        <i class="text-[16px] fa-brands" :class="link.logo"></i>
    </a>
  </div>
</template>

<script setup>
const links = [
  { name: "facebook", url: "https://www.facebook.com/profile.php?id=61577639055138", logo:"fa-facebook"},
  { name: "linkedin", url: "https://www.linkedin.com/in/rex-xyriel-limpangog-08467033a/", logo:"fa-linkedin-in"},
  { name: "github", url: "https://github.com/r-limpz", logo:"fa-github"},
]
</script>


<script>
export default {
    name: "Socials"
}
</script>