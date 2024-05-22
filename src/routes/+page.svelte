<script lang="ts">
  import BackgroundForegroundExample from '$lib/components/BackgroundForegroundExample.svelte'
  import CardExample from '$lib/components/CardExample.svelte'
  import DarkModeSwitch from '$lib/components/DarkModeSwitch.svelte'
  import InputExample from '$lib/components/InputExample.svelte'
  import MutedExample from '$lib/components/MutedExample.svelte'
  import PrimaryExample from '$lib/components/PrimaryExample.svelte'
</script>

<div>
  <header class="flex items-center justify-between">
    <h1 class="mb-6 py-4 text-xl font-bold uppercase">shadcn-svelte theme generator</h1>
    <DarkModeSwitch />
  </header>
  <div class="flex gap-8">
    <BackgroundForegroundExample />
    <PrimaryExample />
    <InputExample />
    <CardExample />
    <MutedExample />
  </div>
</div>
