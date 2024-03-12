
<script lang="ts">
   
    import * as Card from "$lib/components/ui/card/index.js";
    export let  image: string;
    export let  description: string;
     
  </script>

    <div class="  flex-wrap max-w-[344px] w-[344px] border rounded-xl ">
     <img src={image} alt="image" class="rounded-xl">
      <div  class="description max-w-[344px] w-[344px] h-[90px] p-[24px] font-normal text-[14px] ">
        <p  class="description max-w-[296px] w-[294px] h-[45px] ">{description}</p>
      </div>
   
    </div>

