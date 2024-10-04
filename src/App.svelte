<!-- DEPENDENCIES -->
<!-- npm i degit -->
<!-- npm install -->


<!-- How to create a new svelte project: -->
<!-- degit sveltejs/template [project-name]-->

<!-- alternative way -->
<!-- npx degit sveltejs/template [project-name] -->
<!---------------------------------------------->

<!-- HOW TO START SERVER: -->
<!-- npm run build -->
<!-- npm run dev -->


<!-- JAVASCRIPT -->
<script>
	 let Color = ("Red"); //color

	 //Functions:---------
	 const setColor = function(name){
		//Will set/update the color variable
		if (Color !== name){
			Color = name;
		}
	 }

	 const randomColor = function(){
		//Will generate a random color
		const red = Math.round(Math.random() * 255)
		const blue = Math.round(Math.random() * 255)
		const green = Math.round(Math.random() * 255)
		//-0-0-0-0--
		const newColor = `rgb(${red}, ${green}, ${blue})`
		Color = newColor
	 }

</script>

<!-- HTML -->
<main>
	<h3 id="title">Color Flipper</h3>
	<h4 class="desc">Choose a button below to change the color of the circle</h4>
	<div id="colorFlipper" style="background-color: {Color}"></div>
	<div class="buttonHolder">
		<button id="red" on:click={()=>{setColor("Red")}}>Red</button>
		<button id="green" on:click={()=>{setColor("Green")}}>Green</button>
		<button id="yellow" on:click={()=>{setColor("Yellow")}}>Yellow</button>
		<button id="blue" on:click={()=>{setColor("Blue")}}>Blue</button>
		<button id="random" on:click={()=>{randomColor()}} style="font-weight: 500">Random</button>
	</div>
</main>

<!-- CSS -->
<style>
	main{
		display:flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		
	}
	#title{
		font-size: 1.5vw;
	}
	.desc{
		margin-top: -1%;
		font-weight: 400;
		font-size: 0.7vw;
		margin-bottom: 3%;
	}
	#colorFlipper{
		width: 17%;
		height: 15vw;
		border-radius: 100%;
		box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
		margin-bottom: 3%;
		transition: background-color 0.5s ease; 
	}
	.buttonHolder{
		display:flex;
		justify-content: center;
		align-items: center;

		width: 30vw;
		font-size: 100%;
	}
	#green {
		font-weight: 500;
		background-color: green;
		color: rgb(104, 241, 70)
	}

	#red {
		font-weight: 500;
		background-color: red;
		color: rgb(128, 6, 6)
	}

	#yellow {
		font-weight: 500;
		background-color: yellow;
		color: rgb(140, 155, 7)
	}

	#blue {
		font-weight: 500;
		background-color: blue;
		color: rgb(34, 168, 202)
	}

	button {
		border-radius: 5px;
		width: 100px;
		height: 40px;
		margin: 5px;
	}
</style>

<!-- https://www.youtube.com/watch?v=2ml4x0rO1PQ -->