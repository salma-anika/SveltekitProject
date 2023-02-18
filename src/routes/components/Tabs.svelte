
<script>


  import RSS from '../../icons/rss.svelte';
import Pin from '../../icons/pin.svelte';
import HomeAlt from '../../icons/homeAlt.svelte';
import Hat from '../../icons/hat.svelte';
import More from '../../icons/more.svelte';
import SuitCase from '../../icons/suitCase.svelte';
import Intro from './Intro.svelte';

const [toggleState, setToggleState] = useState(1);

const toggleTab = (/** @type {number} */ index) => {
  setToggleState(index);
};
</script>

    <div class="container max-[450px]:flex-col max-[450px]:px-52">
      <div class="bloc-tabs flex-col max-[450px]:text-[26px]  max-[450px]:w-[850px] max-[450px]:ml-[14rem]">
        <button
        class={toggleState === 1 ? "tabs active-tabs" : "tabs"}
        on:click={() => toggleTab(1)}
        >
          Overview
        </button>
        <button
          class={toggleState === 2 ? "tabs active-tabs" : "tabs"}
          on:click={() => toggleTab(2)}
        >
          Work and education
        </button>
        <button
        class={toggleState === 3 ? "tabs active-tabs" : "tabs"}
        on:click={() => toggleTab(3)}
        >
          Places lived
        </button>
        <button
        class={toggleState === 4 ? "tabs active-tabs" : "tabs"}
        on:click={() => toggleTab(4)}
        >
          Contact and basic info
        </button>
        <button
        class={toggleState === 5 ? "tabs active-tabs" : "tabs"}
        on:click={() => toggleTab(5)}
        >
          Details about you
        </button>
      </div>

      <div class="content-tabs max-[450px]:text-[26px]  max-[450px]:w-[850px] max-[450px]:ml-[14rem] max-[450px]:mt-2">
        <div
        class={toggleState === 1 ? "content  active-content" : "content"}
        >
       <Intro/>
        </div>

        <div
        class={toggleState === 2 ? "content  active-content" : "content"}
        >
        
        <div class="shadow-fb rounded w-full bg-white p-4">
   
   <div class="mt-1 flex items-start ">
     <SuitCase />
     <span class="ml-2 ">
       Astha IT Limited Bangladesh{' '}

     </span>
     <div class=' items-end  justify-end ml-[385px] '> <More /></div>
   </div>
   <div class="mt-4 flex items-center">
     <Hat />
     <span class="ml-2">Studied at Bangladesh Army University </span>
     <div class=' items-end justify-end ml-[315px]'> <More/></div>
   </div>
   <div class="mt-4 flex items-center">
     <Hat />
     <span class="ml-2">Intern at Sun IT Limited Rajshahi </span>
     <div class=' items-end justify-end ml-[360px]'> <More/></div>
   </div>
   </div>
        </div>

        <div
        class={toggleState === 3 ? "content  active-content" : "content"}
        >
      
      <div class="shadow-fb rounded w-full bg-white p-4">
   
 
   <div class="mt-4 flex items-center">
     <HomeAlt />
     <span class="ml-2">
       Lives in <b>Rajshahi</b>, Bangladesh{' '}
     </span>
     <div class=' items-end justify-end ml-[380px]'> <More /></div>
   </div>
   <div class="mt-4 flex items-center">
     <Pin />
     <span class="ml-2">
       From  <b>Rajshahi</b>, Bangladesh{' '}
     </span>
     <div class=' items-end ml-[393px] justify-end '> <More/></div>
   </div>

        </div>
        </div>

        <div
        class={toggleState === 4 ? "content  active-content" : "content"}
        >
     
     <div class="shadow-fb rounded w-full bg-white p-4">
   
   <div class="mt-1 flex items-start ">
     <SuitCase />
     <span class="ml-2 ">
       Astha IT Limited Bangladesh{' '}

     </span>
     <div class=' items-end  justify-end ml-[385px] '> <More/></div>
   </div>
   <div class="mt-4 flex items-center">
     <Hat />
     <span class="ml-2">Studied at Bangladesh Army University </span>
     <div class=' items-end justify-end ml-[315px]'> <More/></div>
   </div>
   <div class="mt-4 flex items-center">
     <Hat />
     <span class="ml-2">Intern at Sun IT Limited Rajshahi </span>
     <div class=' items-end justify-end ml-[360px]'> <More/></div>
   </div>
   <div class="mt-4 flex items-center">
     <HomeAlt />
     <span class="ml-2">
       Lives in <b>Rajshahi</b>, Bangladesh{' '}
     </span>
     <div class=' items-end justify-end ml-[380px]'> <More/></div>
   </div>
   <div class="mt-4 flex items-center">
     <Pin />
     <span class="ml-2">
       From  <b>Rajshahi</b>, Bangladesh{' '}
     </span>
     <div class=' items-end ml-[393px] justify-end '> <More /></div>
   </div>
   <div class="mt-4 flex items-center">
     <RSS />
     <span class="ml-2">
       Followed by <b>97 people</b> {' '}
     </span>
     <div class=' items-end ml-[420px] justify-end '> <More /></div>
   </div>
   </div>
        </div>

        <div
        class={toggleState === 5 ? "content  active-content" : "content"}
        >
     
        <Intro/>
        </div>


      </div>
  
    </div>
 
