<script module lang="ts">
  export const metadata = {
    title: 'Web Colaborativa Barrial de Punta Mogotes',
    description: 'Un espacio donde estamos todos en el mismo equipo',
  }

  // import mogotes from '../photos/mogotes.png'
  import mogotes from '../photos/mogotes.png?width=100;250;500&format=webp&srcset'
  import mogotesMeta from '../photos/mogotes.png?as=meta:height;width'
  import OptimizedImg from '@/substrates/toroid-web/components/OptimizedImg.svelte'

  let s = 1.5
</script>

<div class="relative">
  <div class="absolute w-full -top-2 bottom-0 saturate-70">
    <OptimizedImg
      src={mogotes}
      meta={mogotesMeta}
      alt="Ilustracion aerea"
      class="w-full h-full object-cover"
    />
  </div>

  <div class="max-w-screen-sm mx-auto text-white p6 relative">
    <!-- <div class="bg-[#d3895e] h-24"></div> -->
    <div
      class="bg-black/40 rounded-8 b b-3 b-white outline outline-3 outline-black/20 backdrop-blur-sm"
    >
      <h1
        class="text-12 xs:text-16 sm:text-20 font-serif text-center text-shadow-[0_1.5px_0_#000]"
        >Punta Mogotes</h1
      >
      <p class="text-center mb6 text-6 xs:text-8 lh-12 font-serif"
        >Web Barrial Colaborativa</p
      >
      <p class="font-mono text-center pb6 italic"
        >Estamos tod@s en el mismo equipo</p
      >
    </div>

    <!--
  <p class="text-center mb6 text-5 lh-12 font-mono whitespace-nowrap"
    >Amor • Cooperación <span class="hidden sm:inline">•</span><br
      class="sm:contents"
    /> Posibilidades • Evolución</p
  >

  <p class="text-center mb6 font-sans">
    Nos organizamos sin banderas, sin marcas, sin branding<br />
    En servicio del amor a nuestros hijos e hijas<br />
    En servicio del amor a nuestros hermanos y hermanas<br />
    En servicio del amor a Gaia-Tierra-Pachamama<br />
    En servicio del amor a nuestros cuerpos que son de ella<br />
    <br />
    Esta es tu invitación
  </p>

  <div class="max-w-30 mx-auto mb6 relative">
    <OptimizedImg class="w-full" src={tierra} meta={tierraMeta} alt="Tierra" />
  </div> -->
  </div>
</div>
