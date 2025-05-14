<script>
  import ColorPalette from "$lib/ColorPalette.svelte";

  const time = new Date(Date.now()).getFullYear() - 2022;

  let background = $state("gray");
</script>

<div
  style:background-color={`var(--color-${background}-900)`}
  class="flex items-center justify-center min-h-screen p-6"
>
  <div
    class="bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl shadow-xl p-8 max-w-xl w-full text-center space-y-6"
  >
    <h1 class="text-5xl font-extrabold text-red-500 animate-pulse">
      yo, meet a dev.
    </h1>

    <h2 class="text-lg text-white">
      shipping vibes & code for over <span class="font-semibold">{time}</span> years.
    </h2>

    <div class="rounded-xl overflow-hidden border border-white/10 shadow-lg">
      <video
        src="/sharingan.mp4"
        autoPlay
        loop
        muted
        class="w-full object-cover h-64"
      ></video>
    </div>

    <h3 class="text-base leading-relaxed text-white">
      <span class="font-semibold italic text-pink-400">who, fr?</span>
      chasing OSS dreams & building stuff that doesn&apos;t break when it scales.
      real talk.
    </h3>

    <p class="text-sm text-gray-400">
      Get lost at <a
        href="https://iflyrich.space"
        class="underline hover:text-white transition">iflyrich.space</a
      > — infinite loop vibes, no escape 🤘
    </p>

    <ColorPalette bind:background />
  </div>
</div>

<!-- <style lang>
  @reference "tailwindcss";
  :global(html) {
    background-color: theme(--color-background-900);
  }
</style> -->
