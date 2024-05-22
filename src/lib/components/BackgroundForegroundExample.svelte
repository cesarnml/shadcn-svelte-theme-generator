<script>
  import { Input } from '$lib/components/ui/input'
  import { Label } from '$lib/components/ui/label'
  import { hexToHSL } from '$lib/utils/hexToHsl'

  let foreground = ''
  let background = ''

  const updateBackgroundColor = () => {
    document.documentElement.style.setProperty('--background', hexToHSL(background))
  }

  const updateForegroundColor = () => {
    document.documentElement.style.setProperty('--foreground', hexToHSL(foreground))
  }
</script>

<div>
  <h2 class="mb-2 font-mono text-lg font-semibold">Background/Foreground</h2>
  <div class="flex flex-col gap-4">
    <div class="flex justify-between gap-4">
      <div class="flex-grow">
        <Label>Background</Label>
        <Input type="color" bind:value={background} on:input={updateBackgroundColor} />
      </div>
      <div>
        <Label>Foreground</Label>
        <Input type="color" bind:value={foreground} on:input={updateForegroundColor} />
      </div>
    </div>
  </div>
</div>
