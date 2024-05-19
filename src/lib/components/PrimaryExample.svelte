<script>
  import { Button } from '$lib/components/ui/button'
  import { Input } from '$lib/components/ui/input'
  import { Label } from '$lib/components/ui/label'
  import { hexToHSL } from '$lib/utils/hexToHsl'

  let primaryForeground = ''
  let primary = ''

  const updatePrimaryColor = () => {
    document.documentElement.style.setProperty('--primary', hexToHSL(primary))
  }

  const updatePrimaryForegroundColor = () => {
    document.documentElement.style.setProperty('--primary-foreground', hexToHSL(primaryForeground))
  }
</script>

<div>
  <h2 class="mb-2 font-mono text-lg font-semibold">Button and Div</h2>
  <div class="mb-4 flex flex-col gap-2">
    <div class="bg-primary text-center text-primary-foreground">Hello</div>
    <Button>Example</Button>
  </div>
  <div class="flex justify-between gap-4">
    <div class="flex-grow">
      <Label>Primary</Label>
      <Input type="color" bind:value={primary} on:input={updatePrimaryColor} />
    </div>
    <div>
      <Label>Primary Foreground</Label>
      <Input type="color" bind:value={primaryForeground} on:input={updatePrimaryForegroundColor} />
    </div>
  </div>
</div>
