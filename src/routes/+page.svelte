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
  import ReusableSwitch from '$lib/components/ReusableSwitch.svelte'
  import ReusableTable from '$lib/components/ReusableTable.svelte'
  import ReusableToggleGroup from '$lib/components/ReusableToggleGroup.svelte'
  import ReusableTooltip from '$lib/components/ReusableTooltip.svelte'
</script>

<div class="container">
  <header class="mb-6 flex items-center justify-between">
    <h1 class="text-xl font-bold uppercase">shadcn-svelte theme generator</h1>
    <DarkModeSwitch />
  </header>
  <div class="grid grid-cols-10 gap-8">
    <div class="col-span-2">
      <div class="flex flex-col gap-8">
        <BackgroundForegroundExample />
        <PrimaryExample />
      </div>
    </div>
    <div class="col-span-2">
      <div class="flex flex-col gap-8">
        <InputExample />
        <div class="w-fit">
          <div class="flex gap-4">
            <ReusableAvatar />
            <ReusableTooltip />
          </div>
        </div>
      </div>
    </div>
    <div class="col-span-4">
      <ReusableTable />
    </div>
    <div class="col-span-2 w-fit">
      <div class="flex flex-col gap-8">
        <ReusableCalendar />
        <ReusableCheckbox />
      </div>
    </div>
    <div class="col-span-3">
      <div class="flex flex-col gap-8">
        <CardExample />
        <div class="flex items-center gap-4">
          <ReusableToggleGroup />
          <ReusableHoverCard />
          <ReusableSlider />
        </div>
      </div>
    </div>
    <div class="col-span-4 w-fit">
      <MutedExample />
    </div>
    <div class="col-span-3">
      <div class="flex flex-col gap-8">
        <ReusableAccordion />
        <ReusableAlert />
        <div class="flex gap-4">
          <div class="w-fit">
            <ReusableAlertDialog />
          </div>
          <ReusableMenuBar />
        </div>
        <div class="flex items-start gap-4">
          <div class="w-fit">
            <ReusableBadge />
          </div>
          <ReusableSwitch />
        </div>
        <div class="flex flex-col gap-8">
          <ReusableRadioGroup />
        </div>
      </div>
    </div>
  </div>
</div>
