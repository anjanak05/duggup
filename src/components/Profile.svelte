<script>
     import * as Avatar from "$lib/components/ui/avatar";
     const profileData = {
    companyName: "duggup",
    logo_icon: "Logo_icon.png",
    coFounder_avatar: "founder_avatar.png",
    coFounder_Name: "Krishna Kiran",
    designation: "Co-Founder and CEO",
    link_external:"link-external.png",
    Summary:"Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.",
    
   
  };

  // Fetching data from JSON
  const {
    companyName,
    logo_icon,
    coFounder_avatar,
    coFounder_Name,
    designation,
    link_external,
    Summary,  
  } = profileData;
</script>
  <!-- profile component -->

<div  class="max-w-[1424px] w-[1424px] h-[200px] mb-[3%] relative w-full flex flex-wrap items-center gap-[2%] justify-center"  >
    <div class="border w-[120px] h-[120px]">
            <img src="founder_avatar.png" alt="coFounder_Name" >
              <p class="mt-[15px] w-[128px] h-[56px]  text-[24px] font-bold text-center">{coFounder_Name}</p>
         
    </div>
      <div class= " max-w-[834px] w-[834px] relative block w-full border-red-500 mt-[4%]">
        <div class="max-w-[834px] w-[834px] h-[82px] flex justify-between">
            <p class=" w-[584px] h-[72px] text-[14px] font-normal leading-6">{Summary}</p>
            <div class=" w-[140px] h-[82px] text-[14px] font-normal leading-6 text-end">
                <img class="w-[36px] h-[36px] ml-auto rounded-full" src={logo_icon} alt={companyName} />
                <p class="text-[16px]">{companyName}</p>
                <p class="text-[12px]">{designation}</p>

            </div>

        </div>
        <div class="max-w-[834px] w-[834px] h-[36px] flex  justify-between mt-[1%]">
             <button class="flex w-[91px] h-[36px]  justify-center items-center p-[8px] buttonPost rounded">Follow</button>
      <div class="max-w-[174px] w-[174px] h-[28px] flex items-center justify-end">
        <p class="max-w-[115px] w-[115px] h-[20px] flex items-center justify-center gap-[5px]"><span class="text-[14px] font-normal leading-6">My Website</span><img class="w-[12.8px] h-[12.8px]" src={link_external} alt="link_external"> </p>
        <img class=" w-[22.4px] h-[5.6px]" src="dots_icon.png" alt="dotsIcon">
      </div>
        </div>
           
      </div>
</div>
