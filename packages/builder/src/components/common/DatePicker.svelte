<script>
  import Flatpickr from "svelte-flatpickr"
  import { Label, DatePicker } from "@budibase/bbui"

  export let label
  export let value

  function onChange(event) {
    const [selectedDates] = event.detail
    value = selectedDates[0]
  }
</script>

<DatePicker {label} on:change={onChange} {value} />
