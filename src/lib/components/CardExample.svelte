<script>
  import ReusableCard from '$lib/components/ReusableCard.svelte'
  import { Input } from '$lib/components/ui/input'
  import { Label } from '$lib/components/ui/label'
  import { hexToHSL } from '$lib/utils/hexToHsl'

  let cardForeground = ''
  let card = ''

  const updateCardColor = () => {
    document.documentElement.style.setProperty('--card', hexToHSL(card))
  }

  const updateCardForegroundColor = () => {
    document.documentElement.style.setProperty('--card-foreground', hexToHSL(cardForeground))
  }
</script>

<div>
  <h2 class="mb-2 font-mono text-lg font-semibold">Card</h2>
  <ReusableCard />
  <div class="flex justify-between gap-4">
    <div class="flex-grow">
      <Label>Card</Label>
      <Input type="color" bind:value={card} on:input={updateCardColor} />
    </div>
    <div>
      <Label>Card Foreground</Label>
      <Input type="color" bind:value={cardForeground} on:input={updateCardForegroundColor} />
    </div>
  </div>
</div>
