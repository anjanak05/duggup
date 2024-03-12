
<script lang="ts">
   
    import * as Card from "$lib/components/ui/card/index.js";
   
        export let  description: string;
         console.log(description)
  </script>
<Card.Root class="w-[380px]">
    <Card.Content class="grid gap-4">

        <Card.Description>{description}</Card.Description>
   
    </Card.Content>

  </Card.Root>