<script>
  let className = "";
  export let innerClass = "";
  export { className as class };
</script>

<div class={className}>
  <div class="relative group m-1">
    <div
      class="absolute -inset-0.5 bg-gradient-to-r from-pink-600 to-purple-700 rounded-lg blur opacity-75 group-hover:opacity-100 transition duration-1000 group-hover:duration-200 animate-tilt"
    />
    <div class="relative px-4 py-4 bg-indigo-700 rounded-lg leading-none">
      <div class={innerClass}>
        <slot />
      </div>
    </div>
  </div>
</div>
