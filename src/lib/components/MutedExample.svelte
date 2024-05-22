<script>
  import ReusableSkeleton from '$lib/components/ReusableSkeleton.svelte'
  import ReusableSwitch from '$lib/components/ReusableSwitch.svelte'
  import ReusableTabs from '$lib/components/ReusableTabs.svelte'
  import { Input } from '$lib/components/ui/input'
  import { Label } from '$lib/components/ui/label'
  import { hexToHSL } from '$lib/utils/hexToHsl'

  let mutedForeground = ''
  let muted = ''

  const updateMutedColor = () => {
    document.documentElement.style.setProperty('--muted', hexToHSL(muted))
  }

  const updateMutedForegroundColor = () => {
    document.documentElement.style.setProperty('--muted-foreground', hexToHSL(mutedForeground))
  }
</script>

<div>
  <h2 class="mb-2 font-mono text-lg font-semibold">Muted</h2>
  <div class="flex flex-col gap-4">
    <div class="flex flex-col gap-4">
      <ReusableSkeleton />
      <ReusableSwitch />
      <ReusableTabs />
    </div>
    <div class="flex justify-between gap-4">
      <div class="flex-grow">
        <Label>Muted</Label>
        <Input type="color" bind:value={muted} on:input={updateMutedColor} />
      </div>
      <div>
        <Label>Muted Foreground</Label>
        <Input type="color" bind:value={mutedForeground} on:input={updateMutedForegroundColor} />
      </div>
    </div>
  </div>
</div>
