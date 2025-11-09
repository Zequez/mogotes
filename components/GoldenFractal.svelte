<script lang="ts">
  let props: { depth: number } = $props()

  let arr = $derived(Array(props.depth).fill(''))
  let P = 1.618

  let sqrPos = {
    0: 'top-0 left-0',
    1: 'right-0 top-0',
    2: 'bottom-0 left-0',
    3: 'top-0 left-0',
  }

  let rectPos = {
    0: 'bottom-0 right-0',
    1: 'bottom-0 left:0',
    2: 'top-0 left-0',
    3: 'right-0 top-0',
  }
</script>

{#snippet sponsorSqr()}
  <div class="w-1/2 h-1/2 p1">
    <div class="w-full h-full b-3 b-dashed rounded-2 b-gray-400 bg-gray-300"
    ></div>
  </div>
{/snippet}

{#snippet sqr(hv: 'h' | 'v', pos: string)}
  <div
    style={hv === 'h' ? `width: ${100 / P}%` : ''}
    class={[
      {
        'w-full pt-100%': hv === 'v',
        'h-full': hv === 'h',
      },
      'absolute',
      pos,
    ]}
  >
    <div class="absolute inset-0 flex flex-wrap">
      {@render sponsorSqr()}
      {@render sponsorSqr()}
      {@render sponsorSqr()}
      {@render sponsorSqr()}
      <!-- <div class="w-full h-full b-3 b-dashed rounded-2 b-gray-400 bg-gray-300">
        <div></div>
      </div> -->
    </div>
  </div>
{/snippet}

{#snippet golden(hv: 'h' | 'v', depth: number)}
  {#if depth < props.depth}
    {@const thisSqrPos = sqrPos[(depth % 4) as 0 | 1 | 2 | 3]}
    {@const thisRectPos = rectPos[(depth % 4) as 0 | 1 | 2 | 3]}
    <div
      style={hv === 'h'
        ? `padding-top: ${(1 / P) * 100}%`
        : `width: ${(1 - 1 / P) * 100}%`}
      class={[
        {
          'w-full': hv === 'h',
          'h-full': hv === 'v',
        },
        ` bg-black/0 absolute`,
        thisRectPos,
      ]}
    >
      <div class="absolute inset-0">
        {@render sqr(hv, thisSqrPos)}
        {@render golden(hv === 'h' ? 'v' : 'h', depth + 1)}
      </div>
    </div>
  {/if}
{/snippet}

<div style={`padding-top: ${100 * P}%`} class={`w-full relative`}>
  <!-- {#each arr as k, i (i)} -->
  {@render sqr('v', sqrPos[0])}
  {@render golden('h', 1)}
  <!-- {/each} -->
</div>
