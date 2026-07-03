<script lang="ts">
  let { children } = $props();

  let count = $state(0);
</script>

<section
  class="mx-auto mt-5 w-full max-w-4xl rounded-3xl border border-pink-200 bg-linear-to-br from-pink-50 via-yellow-50 to-sky-50 p-6 shadow-[0_20px_60px_rgba(244,114,182,0.18)] ring-1 ring-white/70 sm:p-8"
>
  <div class="mb-5 flex items-center justify-between gap-3">
    <div class="flex items-center gap-3">
      <div
        class="flex h-12 w-12 items-center justify-center rounded-2xl bg-linear-to-br from-pink-500 to-rose-400 text-2xl shadow-lg shadow-pink-200/60"
      >
        ⭐
      </div>

      <div>
        <p
          class="text-xs font-semibold uppercase tracking-[0.32em] text-pink-500"
        >
          For kids
        </p>
        <h2 class="text-2xl font-bold text-slate-800 sm:text-3xl">
          Fun learning card
        </h2>
      </div>
    </div>

    <button
      type="button"
      class="inline-flex items-center gap-2 rounded-full bg-sky-500 px-4 py-2 text-sm font-semibold text-white shadow-md shadow-sky-200 transition hover:-translate-y-0.5 hover:bg-sky-600 active:translate-y-0"
      onclick={() => (count += 1)}
      aria-label="Increase counter"
    >
      Count <span class="min-w-5 text-center">{count}</span>
    </button>
  </div>

  <div
    class="rounded-2xl bg-white/80 p-4 shadow-inner shadow-white/60 ring-1 ring-pink-100 sm:p-6"
  >
    {@render children?.()}
  </div>

  <div class="mt-5 flex items-center justify-between text-sm text-slate-500">
    <span>Made for bright ideas and happy moments.</span>
    <span
      class="rounded-full bg-yellow-200 px-3 py-1 font-medium text-yellow-900"
      >New</span
    >
  </div>
</section>
