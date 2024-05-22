<script lang="ts">
  import BackgroundForegroundExample from '$lib/components/BackgroundForegroundExample.svelte'
  import CardExample from '$lib/components/CardExample.svelte'
  import DarkModeSwitch from '$lib/components/DarkModeSwitch.svelte'
  import InputExample from '$lib/components/InputExample.svelte'
  import MutedExample from '$lib/components/MutedExample.svelte'
  import PrimaryExample from '$lib/components/PrimaryExample.svelte'
  import ReusableAccordion from '$lib/components/ReusableAccordion.svelte'
  import ReusableAlert from '$lib/components/ReusableAlert.svelte'
  import ReusableAlertDialog from '$lib/components/ReusableAlertDialog.svelte'
  import ReusableAvatar from '$lib/components/ReusableAvatar.svelte'
  import ReusableBadge from '$lib/components/ReusableBadge.svelte'
  import ReusableCalendar from '$lib/components/ReusableCalendar.svelte'
  import ReusableCheckbox from '$lib/components/ReusableCheckbox.svelte'
  import ReusableHoverCard from '$lib/components/ReusableHoverCard.svelte'
  import ReusableMenuBar from '$lib/components/ReusableMenuBar.svelte'
  import ReusableRadioGroup from '$lib/components/ReusableRadioGroup.svelte'
  import ReusableSlider from '$lib/components/ReusableSlider.svelte'
  import ReusableTable from '$lib/components/ReusableTable.svelte'
  import ReusableToggleGroup from '$lib/components/ReusableToggleGroup.svelte'
  import ReusableTooltip from '$lib/components/ReusableTooltip.svelte'
</script>

<div>
  <header class="flex items-center justify-between">
    <h1 class="mb-6 text-xl font-bold uppercase">shadcn-svelte theme generator</h1>
    <DarkModeSwitch />
  </header>
  <div class="flex flex-col gap-10">
    <div class="flex gap-8">
      <BackgroundForegroundExample />
      <PrimaryExample />
      <InputExample />
      <CardExample />
      <MutedExample />
    </div>
    <div class="flex gap-8">
      <ReusableAccordion />
      <ReusableAlert />
      <ReusableAlertDialog />
    </div>
    <div class="flex gap-8">
      <ReusableCalendar />
      <ReusableTable />
    </div>
    <div class="flex gap-8">
      <ReusableCheckbox />
      <ReusableBadge />
      <ReusableAvatar />
      <ReusableHoverCard />
      <ReusableMenuBar />
      <ReusableRadioGroup />
    </div>
    <div class="flex gap-8">
      <ReusableSlider />
      <ReusableToggleGroup />
      <ReusableTooltip />
    </div>
  </div>
</div>
