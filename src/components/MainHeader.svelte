<script>
  import Button from "$lib/components/ui/button/button.svelte";
  import * as Avatar from "$lib/components/ui/avatar";
  const headerData = {
    companyName: "duggup",
    logo_icon: "Logo_icon.png",
    coFounder_avatar: "founder_avatar.png",
    coFounder_Name: "Krishna Kiran",
    buttonName: "Post",
    buttonIcon:"Post_icon.png",
    linksIcons: [
      { icons: "Home_icon.png", link_name: "Home" },
      { icons: "Explore_icon.png", link_name: "Explore" },
      { icons: "Learn_icon.png", link_name: "Learn" },
    ],
  };

  // Fetching data from JSON
  const {
    companyName,
    logo_icon,
    coFounder_avatar,
    coFounder_Name,
    buttonName,
    buttonIcon,
    linksIcons,
  } = headerData;
</script>

  <!-- Header for Home page -->
  <div
    class="max-w-[1424px] w-[1424px] h-[73px] mx-auto w-full flex items-center justify-between p-4 py-6 border-dotted border-b"
  >
    <Button class="w-[108px] h-[27px] gap-[4px]"><img class="w-[76px] h-[21px]" src={logo_icon} alt={companyName} />{companyName}</Button>

    <div  class="flex max-w-[749px] w-full flex items-center justify-between">
      <div class="  flex flex-row w-[461px] justify-between">
        <ul class=" headerLinks flex flex-row w-[319px]">
          {#each linksIcons as link}

            <li class="flex w-[112px] h-[36px] justify-center items-center p-[8px] " >
              <img class="p-[4px]" src={link.icons} alt={link.link_name} />
              <span class="p-[8px] text-sm">{link.link_name}</span>
            </li>
          {/each}
        </ul>
        <p class="flex w-[102px] h-[36px]  justify-center items-center p-[8px] buttonPost rounded">
        <img class="p-[4px]" src={buttonIcon} alt=buttonName} />
        <span class="p-[8px]">{buttonName}</span>
        </p>
      </div>
      <a href="ndkn" class="flex w-[248px] h-[52px] justify-between items-center p-[16px] gap-12px">
        <Avatar.Root>
          <Avatar.Image src={coFounder_avatar} alt="@shadcn" />
          <Avatar.Fallback>{coFounder_Name}</Avatar.Fallback>
        </Avatar.Root>
        <p class="w-[128px] h-[24px] gap-[8px] text-[20px] font-medium">{coFounder_Name}</p>
         <img src="chevron-down.png" class="w-[21px] h-[16px] px-[4px]" alt="arrow_down" />
      </a>
      
    </div>
  </div>


