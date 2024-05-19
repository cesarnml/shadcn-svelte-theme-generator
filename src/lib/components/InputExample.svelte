<script lang="ts">
  import ReuseableSelect from '$lib/components/ReuseableSelect.svelte'
  import { Input } from '$lib/components/ui/input'
  import { Label } from '$lib/components/ui/label'
  import { Textarea } from '$lib/components/ui/textarea'
  import { hexToHSL } from '$lib/utils/hexToHsl'

  let input = ''

  const updateInputColor = () => {
    document.documentElement.style.setProperty('--input', hexToHSL(input))
  }
</script>

<div>
  <h2 class="mb-2 font-mono text-lg font-semibold">Borders</h2>
  <div class="flex flex-col gap-4">
    <div class="flex flex-col gap-4">
      <Input />
      <Textarea />
      <ReuseableSelect />
    </div>
    <div class="flex flex-col gap-2">
      <Label class="flex items-center">Input&nbsp;<small>(border)</small></Label>
      <Input type="color" bind:value={input} on:input={updateInputColor} />
    </div>
  </div>
</div>
