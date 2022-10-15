<script>
  import { fade } from "svelte/transition";
  import { inview } from "svelte-inview";

  let isInView;
</script>

<div
  class="wrapper"
  use:inview={{ unobserveOnEnter: true, rootMargin: "-10%" }}
  on:change={({ detail }) => {
    isInView = detail.inView;
  }}
>
  {#if isInView}
    <div in:fade>
      <slot />
    </div>
  {:else}
    <div class="invisible">
      <slot />
    </div>
  {/if}
</div>
