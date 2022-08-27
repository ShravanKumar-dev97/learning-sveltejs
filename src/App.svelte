<script>
	import ContactCard from './ContactCard.svelte'

	let name = "";
	let title = "";
	let paymail = "";
	let imageURL = "";
	

	$: newName = name.toUpperCase();


</script>

<main>
	<div>
		<h1>Hola {newName}!</h1>

		<!-- by default the data flow in svelte is unidirectional -->
		<!-- <input type="text" value="{name}" on:input="{nameInput}" placeholder="Enter your Name"> -->

		<!-- <button on:click="{changeName}">Change Name</button> -->
		<!-- <button on:click="{decrementAge}">Back to Past</button> -->
		<!-- <button on:click="{incrementAge}">Foward to Future</button> -->

		<!-- Two-way Binding  shortcut-->
		<input type="text" bind:value="{name}" placeholder="Enter your Name"> <br>
		<input type="text" bind:value="{title}" placeholder="Job Title"> <br>
		<input type="text" bind:value="{imageURL}" placeholder="Avatar Path"> <br>
		<input type="text" bind:value="{paymail}" placeholder="Wallet paymail">
	</div>

	<br>
	<br>

	<div>
		<ContactCard 
			userName="{name}" 
			jobTitle="{title}"
			userImage="{imageURL}"
			paymail="{paymail}"
		/>
	</div>
	
</main>

<style>
	main {
		/* display: flex; */
		text-align: center;
		padding: 1em;
		/* max-width: 240px; */
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		/* text-transform: uppercase; */
		font-size: 2em;
		font-weight: 200;
	}

	
</style>