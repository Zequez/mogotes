<script lang="ts">
  import '@/center/doc.css'

  const props: { children: any } = $props()
</script>

<div class="max-w-screen-md mx-auto px6 doc pb12">
  {@render props.children?.()}
</div>

<style>
  :global(.doc h1) {
    @apply text-lightblue-400 text-shadow-[0_3px_0_theme('colors.lightblue.700')];
  }
</style>
