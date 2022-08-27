<script>
	import ContactCard from './ContactCard.svelte'

	let name = "Shravan Kumar";
	let age = 25;
	let title = "Developer";
	let description = "I build on BitcoinSV blockchain";
	let imageURL = "https://pbs.twimg.com/profile_images/1491435592722554885/CVjBwy4x_400x400.jpg";
	

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
	<div>
		<h1>Hola {name}!</h1>

		<!-- by default the data flow in svelte is unidirectional -->
		<!-- <input type="text" value="{name}" on:input="{nameInput}" placeholder="Enter your Name"> -->

		<!-- <button on:click="{changeName}">Change Name</button> -->
		<!-- <button on:click="{decrementAge}">Back to Past</button> -->
		<!-- <button on:click="{incrementAge}">Foward to Future</button> -->

		<!-- Two-way Binding  shortcut-->
		<input type="text" bind:value="{name}" placeholder="Enter your Name"> <br>
		<input type="text" bind:value="{title}" placeholder="Job Title"> <br>
		<input type="text" bind:value="{imageURL}" placeholder="Avatar Path"> <br>
		<input type="text" bind:value="{description}" placeholder="Description">
	</div>

	<br>
	<br>

	<div>
		<ContactCard 
			userName="{name}" 
			jobTitle="{title}"
			userImage="{imageURL}"
			description="{description}"
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