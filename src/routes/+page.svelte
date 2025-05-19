<style>
    @keyframes gradientShift {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }
    .animate-gradient {
      background-size: 200% 200%;
      animation: gradientShift 10s ease infinite;
    }
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
    
    let name = $state("July Res - Mis Redes")
    const PLATFORMS = [
      { nombre: "Cafecito - Todas tus fantasías juntas", link: "https://cafecito.app/julires", icon: "☕" },
      { nombre: "Stripchat - No te pierdas mis vivos", link: "https://es.stripchat.com/Julyres_80", icon: "🎥" },
      { nombre: "X - Seguíme en X para mi contenido gratis", link: "https://x.com/julietare28", icon: "𝕏" },
      { nombre: "IG - Para que no te pierdas nada de mi", link: "https://instagram.com/July_res80", icon: "[◉°]" },
      { nombre: "Canal VIP Telegram - Consultame por mi contenido más HOT", link: "https://t.me/julicam4", icon: "🔥" },
      
      
    ]
    </script>
    
    <!-- Background -->
    <div class="min-h-screen bg-gradient-to-b from-pink-500 via-morado-mid to-rose-400 animate-gradient relative">
    
      <Header {name} />
    
      <!-- Profile Picture -->
      <div class="flex justify-center mt-8">
        <img
          src="https://i.ibb.co/qMPXcjdh/imagen-2025-05-08-173630968.png"
          alt="Perfil"
          class="w-32 h-32 rounded-full border-4 border-pink-300 shadow-xl object-cover ring-4 ring-fuchsia-500 hover:ring-pink-400 transition"
        />
      </div>
    
      <!-- Buttons -->
      <div class="py-16 grid gap-y-6 place-items-center px-4">
        {#each PLATFORMS as platform}
          <a
            href={platform.link}
            target="_blank"
            rel="noopener noreferrer"
            class="group shake-on-hover bg-white text-black px-6 py-4 rounded-xl shadow-md w-full max-w-sm flex items-center gap-3 text-center hover:scale-105 hover:shadow-lg transition-transform duration-200 ease-in-out"
          >
            <span class="text-2xl transition-transform duration-200 group-hover:scale-125">{platform.icon}</span>
            <span class="bg-white text-black px-4 py-2 rounded-2xl shadow-md w-full text-center text-sm sm:text-base md:text-lg font-medium transition group-hover:bg-fuchsia-200">
              {platform.nombre}
            </span>
            <span class="text-2xl transition-transform duration-200 group-hover:scale-125">{platform.icon}</span>
          </a>
        {/each}
      </div>
    
      <!-- Floating CTA -->
      <div class="fixed bottom-0.5 left-4 right-4 sm:mx-auto sm:w-fit px-6 py-3 text-white text-center bg-gradient-to-r from-pink-600 to-fuchsia-500 rounded-full shadow-lg text-sm sm:text-base z-50 animate-bounce">
        🔥 ¡No te pierdas mi contenido exclusivo! 🔥
      </div>
    </div>