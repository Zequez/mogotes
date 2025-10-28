<script lang="ts">
  import techo from '../photos/techo2.jpg'
</script>

<div class="relative bg-stone-50 pt6 text-lightblue-800 overflow-hidden">
  <div
    class="absolute z-10 top-0 left-0 w-full h-5 saturate-130 brightness-120 shadow-[0_2px_3px_0_#000a,0_1px_0_0_#0005]"
    style={`background-image: url('${techo}'); background-size: 120px`}
  ></div>
  <slot />
</div>
