<script>
	import ContactCard from './ContactCard.svelte'

	let name = "";
	let age = 25;
	let title = "";
	let description = "";
	

	$: newName = name.toUpperCase();





	function incrementAge (){
		age += 1;
	}

	function decrementAge (){
		if(age>0){
		age -= 1;
		}
	}

	function changeName(){
		name = "Rocky"
		age = 33
	}


	// // for unidirectional method, we have to go with event
	// function nameInput(event) {
	// 	const enteredValue = event.target.value;
	// 	name = enteredValue;
	// }

</script>

<main>
	<h1>Hello {newName}!</h1>

	<!-- by default the data flow in svelte is unidirectional -->
	<!-- <input type="text" value="{name}" on:input="{nameInput}" placeholder="Enter your Name"> -->

	<!-- <button on:click="{changeName}">Change Name</button> -->
	<!-- <button on:click="{decrementAge}">Back to Past</button> -->
	<!-- <button on:click="{incrementAge}">Foward to Future</button> -->

	<!-- Two-way Binding  shortcut-->
	<input type="text" bind:value="{name}" placeholder="Enter your Name"> <br>
	<input type="text" bind:value="{title}" placeholder="Job Title"> <br>
	<input type="text" bind:value="{description}" placeholder="Description">

	<ContactCard 
		userName="{name}" 
		jobTitle="{title}"
		description="{description}"
	/>
	
</main>

<style>
	main {
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