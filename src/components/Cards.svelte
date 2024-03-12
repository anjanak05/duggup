<script lang="ts">
    import { Description } from "$lib/components/ui/card";
import Card from "./Card.svelte";
    const cardData = [
    {
        companyName: "duggup",
        logo_icon: "Logo_icon.png",
        place:"San Francisco Bay Area",
        startDate: "Nov 2023",
        endDate: "Dec 2023",
        designation: "Co-Founder and CEO",
        jobNature: "Full-time • Remote",
        imageDescription: [
            { image: "appleceo_img.png", description: "No amount of technology can convert a bad story into a good story." },
            { image: "man_img.png", description: "Most people don't have original ideas. Here is how Sam Altman pushes himself to have unpopular ideas." },
        
        ]
    },
    {
        companyName: "BetterUp",
        logo_icon: "Logo_icon.png",
        place:"San Francisco Bay Area",
        startDate: "Sep 2022",
        endDate: "Dec 2023",
        designation: "VP Engineering",
        jobNature: "Full-time",
        imageDescription: [
            { image: "lapotp_img.png", description: "Startup Lesson I am reflecting. Don't build for the 'average person'." },
            { image: "reflection_img.png", description: "Your biggest regrets at 80 will be acts of omission." },
        ]
    }
];
export let  description: string;

</script>
   <div  class="max-w-[987px] w-[987px] ml-[5%] mt-[3%] w-full flex items-center justify-left  border border-red-500">
<div class="max-w-[207px] w-[207px] h-[288px] mx-auto w-full flex items-center justify-between border-dotted border-r-[3px]" >

</div>
<div class="max-w-[764px] w-[764px] h-[274px] mx-auto w-full flex items-center justify-between border border-red-500">
    {#each cardData as card}
    <!-- Render the Card component for each object in cardData -->
    {#each  card.imageDescription as title, description}
    <Card
      
        description ={description}

    />
    {/each}
{/each}
</div>
   </div>
   <div class="max-w-[987px] w-[157px] ml-[5%] mt-[3%] w-full flex items-center justify-left  border border-red-500">

   </div>
  