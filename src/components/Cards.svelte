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
        logo_icon: "BetterUp_icon.png",
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
export let  image: string;


</script>
<div class="flex flex-wrap">
{#each cardData as card}
   <div  class="max-w-[987px] w-[987px] ml-[5%]  w-full flex flex items-center justify-between  border border-none">
<div class="text-end max-w-[207px] w-[207px] h-[288px] pr-[2%] flex flex-wrap relative border-dotted border-r-[3px] flex flex-col justify-center " >
<p class="text-[12px] text-[#7A9299]">{card.endDate}</p>

<img class=" max-w-[16px] w-[16px] h-[16px] absolute right-[-10px]" src="Ellipse_small.png" alt="Ellipse_small">

</div>

   
  <!-- Render the Card component for each object in cardData -->
  <div class="max-w-[780px] w-[780px] h-[274px] mx-auto w-full gap-[4px] flex flex-wrap items-center justify-evenly border border-none">
  {#each card.imageDescription as item}
  <Card 
      image={item.image}
      description={item.description}
    />
  {/each}
</div>

   </div>
   <!-- code for experience div -->
   <div class="max-w-[987px] w-[157px] ml-[5%] w-full flex flex-wrap items-center justify-left  border border-none">
<div  class="max-w-[207px] w-[207px] h-[157px] w-full border-dotted border-r-[3px] pr-[2%] text-end flex flex-col justify-center relative">
   
        <img class="w-[36px] h-[36px] ml-auto rounded-full" src={card.logo_icon} alt={card.companyName} />
       <div class="leading-[16px]">
        <p class="text-[16px] font-bold">{card.companyName}</p>
        <p class="text-[12px] text-[#7A9299]">{card.place}</p>
        <p class="text-[12px] text-[#7A9299]">Joined</p>
        <p class="text-[12px] text-[#7A9299]">{card.startDate}</p>
       </div>

<div class="absolute right-[-15px]">
<img class=" max-w-[13px] w-[13px] h-[6px] absolute right-[7px] top-[-236%]" src="chevron_up.png" alt="Ellipse_small">

<img class=" max-w-[28px] w-[28px] h-[27px]  " src="Ellipse_large.png" alt="Ellipse_small">

</div>
   
</div>
<div  class="max-w-[76%] w-[761%] h-[99px] px-[24px] py-[24px] ">
    <div class="max-w-[100%] w-[100%] h-[83px] px-[28px] py-[20px] bg-[#fffafa] rounded-xl">
    <p class="text-[20px] font-bold ">{card.designation}</p>
    <p class="text-[12px] text-[#7A9299] text-[#7A9299]" >{card.jobNature}</p>
</div>
</div>
   </div>
   {/each}
</div>