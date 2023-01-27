<script lang="ts" context="module">
	import '../app.css'
</script>
<script>
	import { Modals, closeModal } from 'svelte-modals';

	import { openModal } from 'svelte-modals';

	import Modal from './Modal.svelte';
	import Theme from './Theme.svelte';
	

	function handleClick() {
		openModal(Modal, {
			
		});
	}
</script>
<Theme/>
<Modals>
	<div slot="svelte-modal" on:click={closeModal} />
</Modals>

<div class=" bg-slate-100 dark:bg-zinc-800 border-b border-slate-200 dark:border-slate-900 max-[450px]:w-fit ">
	<div class=" m-auto flex pt-[100px] max-[450px]:flex-col ">
		<div class="main-left w-[580px] p-[40px]">
			<p class="facebook-logo text-[55px] font-bold mt-[100px] max-[450px]:text-[75px]">facebook</p>

			<p class="facebook-status text-[28px] mt-[10px] text-black max-[450px]:text-[30px] dark:text-white">
				Facebook helps you connect and share with the people in your life.
			</p>
		</div>

		<div class="main-right w-[400px] h-[450px] max-[450px]:w-[550px] max-[450px]:h-[550px] m-auto">
			<div class="main-right-login p-[20px] bg-white rounded-[6px] dark:bg-zinc-700">
				<div class="main-right-email w-[100%] mt-[10px]">
					<input
						type="email"
						placeholder="Email address or phone number"
						class="w-[100%] p-[9px] font-[17px] rounded-[5px] dark:bg-zinc-700 dark:border-slate-200 dark:text-white"
					/>
				</div>

				<div class="main-right-password w-[100%] mt-[20px]">
					<input
						type="password"
						placeholder="Password"
						class="w-[100%] p-[9px] font-[17px] rounded-[5px] dark:bg-zinc-700 dark:border-slate-200 dark:text-white"
					/>
				</div>

				<div class="main-right-button w-[100%] mt-[20px]">
					<button
						class="w-[100%] p-[9px] font-[17px] rounded-[8px] cursor-pointer text-white border-none"
					>
						Log In
					</button>
				</div>

				<div class="main-right-link w-[100%] mt-[20px] text-center">
					<a href="" class="font-[17px] ">Forgotten account?</a>
				</div>

				<div class="main-right-line w-[100%] mt-[20px] h-[1px]" />

				<div class="main-right-account w-[100%] mt-[20px] mt-auto m-[20px]">
					<button
						class="w-[100%] p-[10px] text-[20px] border-none rounded-[10px] text-white cursor-pointer"
						on:click={handleClick}>Create New Account</button
					>
				</div>

				<div class="main-right-page-link w-[400px] mt-[20px] flex justify-center text-[17px]">
					<a href="" class="font-bold text-black dark:text-white">Create a Page </a>
					<p class="ml-[5px] dark:text-white">for a celebrity, band or business.</p>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.facebook-logo {
		color: #1877f2;
	}

	.main-right-login {
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1), 0 8px 16px rgba(0, 0, 0, 0.1);
	}

	.main-right-email input[type='email'] {
		border: none;
		border: 1px solid #ccc;
	}

	.main-right-password input[type='password'] {
		border: none;
		border: 1px solid #ccc;
		border-radius: 5px;
	}

	.main-right-button button {
		border: none;
		background-color: #1877f2;
	}

	.main-right-link a {
		text-decoration: none;
		color: #1877f2;
	}
	.main-right-line {
		border: 1px solid #ccc;
	}

	.main-right-account {
		width: 220px;
	}
	.main-right-account button {
		border: none;
		background-color: #42b72a;
	}

	.main-right-page-link a {
		text-decoration: none;
	}

	.main-right-account {
		width: 220px;
		margin: auto;
		margin-top: 20px;
	}
</style>
