<script lang="ts">
  let { background = $bindable() } = $props();

  const colors = [
    { name: "amber", bg: "bg-amber-900" },
    { name: "gray", bg: "bg-gray-900" },
    { name: "blue", bg: "bg-blue-900" },
  ];

  const getBorderClass = (color: string) =>
    background === color ? "border-gray-300" : "border-transparent";
</script>

<div class="flex gap-2 items-center">
  {#each colors as { name, bg }}
    <button
      aria-label={name}
      onclick={() => (background = name)}
      class={`w-5 h-5 ${bg} border ${getBorderClass(name)} bg- rounded-full`}
    ></button>
  {/each}
</div>
