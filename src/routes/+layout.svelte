<script>
  import { ModeWatcher } from 'mode-watcher'

  import '../app.css'
</script>

<ModeWatcher />
<main class="container grid min-h-screen py-12">
  <slot />
</main>
