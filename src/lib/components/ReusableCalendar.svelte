<script lang="ts">
  import { getLocalTimeZone, today } from '@internationalized/date'
  import { Calendar } from '$lib/components/ui/calendar/'

  let value = today(getLocalTimeZone())
</script>

<Calendar bind:value class="h-fit rounded-md border shadow" />
