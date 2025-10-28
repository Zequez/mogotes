<script lang="ts">
  import guardaTexture from '../photos/wall-stone.png'
</script>

<div id="nav-start"></div>
<a
  href="#nav-start"
  onclick={(ev) => {
    const el = document.getElementById('nav-start')!
    el.scrollIntoView({ behavior: 'smooth', block: 'start' })
    ev.preventDefault()
  }}
  class="h-12 text-center flexcc relative"
  style={`background-image: url(${guardaTexture})`}
>
  <span
    class="absolute inset-0 pointer-events-none shadow-[inset_0_-6px_0_#0007,inset_0_4px_#fffa]"
  ></span>
  <span class="absolute w-full h-1px top-4px bg-white/60"></span>
  <!-- <span
    class="absolute inset-0 pointer-events-none bg-gradient-to-b from-white/5 to-black/5"
  ></span> -->
  <span
    class="relative px3 b b-stone-300 bg-stone-50 rounded-4 text-stone-800 text-shadow-[0_1px_0_#fff] font-serif font-bold text-5 lh-6 py0.6 -mt3px shadow-[inset_0_-4px_5px_0_#0002,0_1px_0_#000a]"
  >
    Mogotes
    <span
      class="bg-stone-400 h3px w3px rounded-full absolute top-1/2 left-5px -translate-y-1/2"
    ></span>

    <span
      class="bg-stone-400 h3px w3px rounded-full absolute top-1/2 right-5px -translate-y-1/2"
    ></span>
  </span>
</a>
