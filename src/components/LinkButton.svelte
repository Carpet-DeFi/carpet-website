<script>
  let className = "";
  export let href;
  export let text = "";
  export { className as class };
</script>

<div class={className}>
  <a
    {href}
    class="px-6 py-3 bg-white rounded-2xl leading-none text-blue-700 uppercase font-semibold text-xl"
  >
    {text}
    <slot />
  </a>
</div>
