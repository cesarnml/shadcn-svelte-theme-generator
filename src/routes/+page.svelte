<script lang="ts">
  import BackgroundForegroundExample from '$lib/components/BackgroundForegroundExample.svelte'
  import CardExample from '$lib/components/CardExample.svelte'
  import InputExample from '$lib/components/InputExample.svelte'
  import MutedExample from '$lib/components/MutedExample.svelte'
  import PrimaryExample from '$lib/components/PrimaryExample.svelte'
</script>

<div>
  <h1 class="mb-6 py-4 text-xl font-bold uppercase">shadcn-svelte theme generator</h1>
  <div class="flex gap-8">
    <BackgroundForegroundExample />
    <PrimaryExample />
    <InputExample />
    <CardExample />
    <MutedExample />
  </div>
</div>
