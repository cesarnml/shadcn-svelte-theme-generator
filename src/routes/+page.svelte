<script lang="ts">
  import { Button } from '$lib/components/ui/button'

  let user: User = {
    email: 'cmejia@gmail.com',
    password: '123',
  }
</script>

<div>
  <h1>shadcn-svelte theme generator</h1>
  <Button>Click me</Button>
  <div>{user.email}</div>
</div>
