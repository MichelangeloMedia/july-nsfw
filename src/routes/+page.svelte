


<style>

@keyframes shake {
  0%, 100% { transform: translateX(0); }
  20%, 60% { transform: translateX(-4px); }
  40%, 80% { transform: translateX(4px); }
}

.shake-on-hover:hover {
    animation: shake 0.5s ease-in-out;
}

</style>

<script>
    
import { injectAnalytics } from '@vercel/analytics/sveltekit'
import Link from './link.svelte'
import Header from './header.svelte'


let name = $state("JULY RES - NSFW")
const PLATFORMS = [
    { nombre : "Cafecito - Todas tus fantasías juntas",
     link: "",
      icon:"☕"},

    { nombre : "Onlyfans - Contenido más exclusivo",
     link: "",
      icon:"🌟"},

    { nombre : "CAM4 - No te pierdas mis vivos ",
     link: "",
      icon:"🎥"},

    { nombre : "X - Seguíme para contenido gratis",
     link: "https://x.com/julietare28",
      icon:"𝕏"},

    { nombre : "Canal VIP Telegram - Sumate para mi contenido más HOT",
     link: "",
      icon:"🔥"}
    
    ]




</script>

<div class="h-screen bg-gradient-to-b from-pink-500 to-grey-200">

    <Header {name} />

      <!-- Profile picture -->
  <div class="flex justify-center mt-6">
    <img
      src="https://i.ibb.co/zHfVnx82/imagen-2025-05-08-170926297.png"
      alt=""
      class="w-32 h-32 rounded-full border-4 border-red-300 shadow-lg object-cover"
    />
  </div>

    <div class="py-20 grid gap-y-6 place-items-center">
        {#each PLATFORMS as platform}
        <a
        href={platform.url}
        target="_blank"
        rel="noopener noreferrer"
        class="shake-on-hover bg-white text-black px-6 py-4 rounded-xl shadow-md w-full max-w-sm
         flex items-center gap-3 text-center  transition duration-100">
      
            <span class="text-2xl">{platform.icon}</span>
            <span class="bg-white text-black px-6 py-4 rounded-2xl shadow-md
            w-full max-w-xs text-center hover:bg-fuchsia-200 transition">{platform.nombre}</span>
            <span class="text-2xl">{platform.icon}</span>
        </a>
        {/each}
    </div>
</div>