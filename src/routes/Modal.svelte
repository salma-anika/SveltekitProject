<script>
	import { closeModal } from 'svelte-modals';
	

	/**
	 * @type {any}
	 */
	export let isOpen;
    
	import { onMount } from 'svelte';
	
    let selected = '2000';
	let options = [
		'2000',
		'2001',
		'2002',
		'2003',
		'2004',
		'2005',
		'2006',
		'2007',
		'2008',
		'2009',
		'2010',
		'2011',
		'2012',
		'2013',
		'2014',
		'2015',
		'2016',
		'2017',
		'2018',
		'2019',
		'2020',
		'2021',
		'2022',
		'2023',
		
	]

	$: console.log('Changed selected:', selected)
	$: console.log('Updated options:', options)

    let selected1 = 'Jan';
	let options1 = [
		'Jan',
		'Feb',
		'March',
		'April',
		'June',
		'July',
		'August',
		'September',
		'October',
        'November',
        'December',
		
	]

	$: console.log('Changed selected:', selected1)
	$: console.log('Updated options:', options1)

    let selected2 = '1';
	let options2 = [
		'1',
		'2',
		'3',
		'4',
		'5',
		'6',
		'7',
		'8',
		'9',
        '10',
        '11',
        '21',
        '22',
        '23',
        '24',
        '25',
        '26',
        '27',
        '28',
        '29',
        '30',
        '31',
		
	]

	$: console.log('Changed selected:', selected1)
	$: console.log('Updated options:', options1)



</script>

{#if isOpen}
	<div class="container w-full h-full bg-slate-100">
		<div
			class="modal w-full h-full top-0 left-0 bottom-0 right-0 fixed">
			<div class="modal-signup w-1/2 m-auto mt-24 bg-white relative rounded-md p-5 shadow-md max-w-[35%]">
				<div class="modal-close absolute text-xl cursor-pointer text-black right-3 top-3" on:click={closeModal}>
					X
				</div>

				<div class="modal-signup-head w-full pb-3 mt-1 text-3xl">
					<p class="modal-signup-name text-3xl font-bold">Sign Up</p>

					<p class="modal-signup-note text-base mt-1">It's quick and easy.</p>
				</div>

				<div class="modal-signup-name w-full flex mt-3 justify-between">
					<input type="text" placeholder="First name" class="w-[48%] p-[8px] text-[17px] rounded-[5px] border-none" />

					<input type="text" placeholder="Surname" class="w-[48%] p-[8px] text-[17px] rounded-[5px] border-none"/>
				</div>

				<div class="modal-signup-email w-full flex mt-3">
					<input type="email" placeholder="Email address or phone number"class="w-[100%] p-[8px] text-[17px] rounded-[5px] border-none" />
				</div>

				<div class="modal-signup-password w-full flex mt-3">
					<input type="password" placeholder="Password" class="w-[100%] p-[8px] text-[17px] rounded-[5px] border-none" />
				</div>

				<div class="modal-date-birth w-full flex mt-3 text-center">
					<label for="">Date of birth</label>

					<div class="modal-date-alert w-4 h-4 inline-block text-xs text-center text-white ml-1 rounded-[50%] ">
						<a>&#63;</a>
					</div>
				</div>
                
				<div class="modal-date-selection w-[100%] flex  mt-[5px]">
					<div class="select-choice w-[33%]">
                        <select name="" id="" bind:value={selected2} class="w-[96%] p-[5px] text-[17px] rounded-[5px] border-none text-black">
                           
                            {#each options2 as value}<option {value}>{value}</option>{/each}
                        </select>
					</div>
					<div class="select-choice w-[33%]">
					
							<select name="" id="" bind:value={selected1} class="w-[96%] p-[5px] text-[17px] rounded-[5px] border-none text-black">
                           
                                {#each options1 as value}<option {value}>{value}</option>{/each}
                            
						</select>
					</div>
					<div class="select-choice w-[33%]">
						<select name="" id="" bind:value={selected} class="w-[96%] p-[5px] text-[17px] rounded-[5px] border-none text-black">
                           
                                {#each options as value}<option {value}>{value}</option>{/each}
                            </select>
							
					</div>
				</div>

				<div class="modal-gender w-full flex text-center mt-3">
					<label for="">Gender</label>

					<div class="modal-gender-alert h-4 w-4 inline-block text-xs text-center text-white ml-1">
						<a>&#63;</a>
					</div>
				</div>

				<div class="modal-gender-choice w-full justify-between flex mt-1">
					<div class="modal-gender-name w-[32%] p-[5px] text-[17px] rounded-[5px] border-none justify-between flex item-aligns-center">
						<label for="radiochoice">Female</label>

						<input type="radio" name="radio" id="radiochoice" />
					</div>

					<div class="modal-gender-name w-[32%] p-[5px] text-[17px] rounded-[5px] border-none justify-between flex item-aligns-center">
						<label for="radiochoice2">Male</label>

						<input type="radio" name="radio" id="radiochoice2" />
					</div>

					<div class="modal-gender-name w-[32%] p-[5px] text-[17px] rounded-[5px] border-none justify-between flex item-aligns-center ">
						<label for="radiochoice3">Custom</label>

						<input type="radio" name="radio" id="radiochoice3" />
					</div>
				</div>

				<div class="modal-signup-terms w-full mt-4 text-xs">
					<p>
						By clicking Sign Up, you agree to our Terms, Data Policy and Cookie Policy. You may
						receive SMS notifications from us and can opt out at any time.
					</p>
				</div>

				<div class="modal-signup-button w-full m-auto mt-5">
					<button on:click={closeModal} class="w-[100%] p-[10px] text-[18px] rounded-[5px] border-none text-white cursor-pointer "> Sign Up</button>
				</div>
			</div>
		</div>
	</div>
{/if}
<style>
     * {
            
            box-sizing: border-box;
            font-family: SFProDisplay-Regular, Helvetica, Arial, sans-serif;
        }
        
        .modal {
            background-color: rgba(250, 250, 250, 0.8);
        }
        .modal-signup {
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1), 0 8px 16px rgba(0, 0, 0, 0.1);
        }
        
        .modal-signup-head {
            border-bottom: 1px solid #ccc;
        }
        
        .modal-signup-name input[type='text'] {
           
            border: 1px solid #ccc;
            background-color: #eee;
        }
        
        .modal-signup-email input[type='email'] {
           
            border: 1px solid #ccc;
            background-color: #eee;
        }
        
        .modal-signup-password input[type='password'] {
            
            border: 1px solid #ccc;
            background-color: #eee;
        }
        
        .modal-date-alert {
            background-color: #aaa;
        }
        .select-choice select {
           
            border: 1px solid #ccc;
            color: #080808;
        }
        
        .modal-gender-alert {
            background-color: #aaa;
            border-radius: 50%;
        }
        
        .modal-gender-name {
            border: 1px solid #ccc;

        }
        
        .modal-signup-button {
            max-width: 200px;
        }
        .modal-signup-button button {
           
            background-color: #32cd32;
           
        }
        
</style>
