<script lang="ts">
  import { Button } from '$lib/components/ui/button'
  import Input from '$lib/components/ui/input/input.svelte'
  import * as Select from '$lib/components/ui/select/'

  import Textarea from '$lib/components/ui/textarea/textarea.svelte'

  const fruits = [
    { value: 'apple', label: 'Apple' },
    { value: 'banana', label: 'Banana' },
    { value: 'blueberry', label: 'Blueberry' },
    { value: 'grapes', label: 'Grapes' },
    { value: 'pineapple', label: 'Pineapple' },
  ]

  let primaryForeground = ''
  let primary = ''
  let input = ''

  $: {
    console.log('buttonPrimaryColor:', primary)
  }

  const hexToHSL = (H) => {
    let r = 0,
      g = 0,
      b = 0
    if (H.length == 4) {
      r = '0x' + H[1] + H[1]
      g = '0x' + H[2] + H[2]
      b = '0x' + H[3] + H[3]
    } else if (H.length == 7) {
      r = '0x' + H[1] + H[2]
      g = '0x' + H[3] + H[4]
      b = '0x' + H[5] + H[6]
    }
    r /= 255
    g /= 255
    b /= 255
    let cmin = Math.min(r, g, b),
      cmax = Math.max(r, g, b),
      delta = cmax - cmin,
      h = 0,
      s = 0,
      l = 0
    if (delta == 0) h = 0
    else if (cmax == r) h = ((g - b) / delta) % 6
    else if (cmax == g) h = (b - r) / delta + 2
    else h = (r - g) / delta + 4
    h = Math.round(h * 60)
    if (h < 0) h += 360
    l = (cmax + cmin) / 2
    s = delta == 0 ? 0 : delta / (1 - Math.abs(2 * l - 1))
    s = +(s * 100).toFixed(1)
    l = +(l * 100).toFixed(1)
    return h + ' ' + s + '% ' + l + '%'
  }
  const updatePrimaryColor = () => {
    document.documentElement.style.setProperty('--primary', hexToHSL(primary))
  }

  const updatePrimaryForegroundColor = () => {
    document.documentElement.style.setProperty('--primary-foreground', hexToHSL(primaryForeground))
  }

  const updateInputColor = () => {
    document.documentElement.style.setProperty('--input', hexToHSL(input))
  }
</script>

<div>
  <h1>shadcn-svelte theme generator</h1>
  <div class="bg-primary text-primary-foreground">Hello</div>
  <Button>Click me</Button>
  <Input type="color" bind:value={primary} on:input={updatePrimaryColor} />

  <Input type="color" bind:value={primaryForeground} on:input={updatePrimaryForegroundColor} />
  <div class="flex flex-col gap-4">
    <h2>Borders</h2>
    <Input />
    <Textarea />
    <Select.Root>
      <Select.Trigger class="w-[180px]">
        <Select.Value placeholder="Select a fruit" />
      </Select.Trigger>
      <Select.Content>
        <Select.Group>
          <Select.Label>Fruits</Select.Label>
          {#each fruits as fruit}
            <Select.Item value={fruit.value} label={fruit.label}>{fruit.label}</Select.Item>
          {/each}
        </Select.Group>
      </Select.Content>
      <Select.Input name="favoriteFruit" />
    </Select.Root>
  </div>
  <hr />
  <Input type="color" bind:value={input} on:input={updateInputColor} />
</div>
