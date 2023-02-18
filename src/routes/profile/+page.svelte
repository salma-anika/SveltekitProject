<script lang="ts">
	import Intro from '../components/Intro.svelte';
    import { Tabscopy, TabList, TabPanel, Tab } from '../components/tabs';

import TimelineHeader from '../components/TimelineHeader.svelte';
import '../../app.css';
import FacebookLogo from '../../icons/facebookLogo.svelte';
import SearchIcon from '../../icons/searchIcon.svelte';
import Home from '../../icons/home.svelte';
import Watch from '../../icons/watch.svelte';
import Groups from '../../icons/groups.svelte';
import Feed from '../../icons/feed.svelte';
import Plus from '../../icons/plus.svelte';
import Messenger from '../../icons/messenger.svelte';
import Bell from '../../icons/bell.svelte';
import SuitCase from '../../icons/suitCase.svelte';
import Hat from '../../icons/hat.svelte';
import HomeAlt from '../../icons/homeAlt.svelte';
import Pin from '../../icons/pin.svelte';
import RSS from '../../icons/rss.svelte';
import More from '../../icons/more.svelte';
</script>
<div>
    <div class="h-14 flex justify-between w-screen shadow-fb px-4 py-2  max-[450px]:text-[26px]">
      <div class="flex">
        <FacebookLogo />
        <div class="h-10 w-64 ml-2 flex items-center rounded-full bg-fFill p-3">
          <SearchIcon />
          <input
          class="text-fGrey ml-2 bg-fFill focus:outline-none"
            placeholder="Search Facebook"
          />
        </div>
      </div>

      <div class="flex space-x-24 items-center max-[450px]:hidden">
        <button class="focus:outline-none">
          <Home />
        </button>
        <button class="focus:outline-none">
          <Watch />
        </button>
        <button class="focus:outline-none">
          <Groups />
        </button>
        <button class="focus:outline-none">
          <Feed />
        </button>
      </div>

      <div class="flex space-x-2">
        <button class="h-9 p-0.5 flex items-center rounded-full focus:outline-none max-[450px]:hidden">
          <img
            src="src/image/pro.jpg"
            class="rounded-full border w-9 border-fButton"
            alt="profile"
          />
          <div class="text-fBlack font-medium ml-2 pr-3">
            Salma Anika
          </div>
        </button>

        <div class="w-10 bg-fButton flex items-center justify-center relative rounded-full max-[450px]:hidden">
          <div class="absolute rounded-full bg-fRed w-5 h-5 z-50 inset-x-6 -top-1 hidden">
            <div class="text-sm text-white text-center">3</div>
          </div>
          <Plus />
        </div>

        <div class="w-10 bg-fButton flex items-center justify-center relative rounded-full max-[450px]:text-[26px] ">
          <div class="absolute rounded-full bg-fRed w-5 h-5 z-50 inset-x-6 -top-1 hidden">
            <div class="text-sm text-white text-center">3</div>
          </div>
          <Messenger />
        </div>
        <div class="w-10 bg-fButton rounded-full flex justify-center items-center relative">
            <div class="absolute rounded-full bg-fRed w-5 h-5 z-50 inset-x-6 -top-1">
              <div class="text-sm text-white text-center">3</div>
            </div>

            <Bell />
          </div>

       
      </div>
      
    </div>
   
    <TimelineHeader/>
    <div class='container px-44'>
        <Tabscopy>
            
            <TabList>
                <Tab>OverView</Tab>
                <Tab> Work and education</Tab>
                <Tab>Places lived</Tab>
                <Tab> Contact and basic info</Tab>
                <Tab>Details about you</Tab>
            </TabList>
        
            <TabPanel>
                <h2 class="content"><Intro/> </h2>
            </TabPanel>
        
            <TabPanel>
                <h2 class="content"> 
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
                             
                             
                </h2>
            </TabPanel>
        
            <TabPanel>
                <h2 class="content">
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
                             
                     
                </h2>
            </TabPanel>
            <TabPanel>
                <h2 class="content">
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
                             
                     
                             
                     
                </h2>
            </TabPanel>
            <TabPanel>
                <h2 class="content">
                    <Intro/>
                             
                     
                </h2>
            </TabPanel>

        </Tabscopy>
        
     
        </div>
       
  </div>
