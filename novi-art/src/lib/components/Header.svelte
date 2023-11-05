<script>
</script>

<body>
	<label>
		<input type="checkbox" />
		<span class="menu"> <span class="hamburger" /> </span>
		<ul>
			<li><a href="/" class="home">Home</a></li>
			<li><a href="/drawings" class="drawings">Drawings</a></li>
			<li><a href="src\routes\videos\+page.svelte" class="videos">Videos</a></li>
			<li><a href="src\routes\installations\+page.svelte" class="installations">Installations</a></li>
			<li><a href="src\routes\performances\+page.svelte" class="performances">Performances</a></li>
			<li><a href="src\routes\contact\+page.svelte" class="contact">Contact</a></li>
			<span style="cursor:pointer"><a href="#top"><img src="src\assets\down-arrow.png" class="arrow" alt="arrow"></a></span>
		</ul>
	</label>
<!--NAV FIXEN, WERKT NIET. Componenten doen het niet. Verwijzing naar home gaat ook verkeerd-->
	<nav>
		<a href="/" class="home">Home</a>
		<a href="/drawings" class="drawings">Drawings</a>
		<a href="src\routes\videos\+page.svelte" class="videos">Videos</a>
		<a href="src\routes\installations\+page.svelte" class="installations">Installations</a>
		<a href="src\routes\performances\+page.svelte" class="performances">Performances</a>
		<a href="src\routes\contact\+page.svelte" class="contact">Contact</a>
	</nav>
</body>

<style>
	
	@media (width>35em) {

		body {
			background-color: rgb(255, 252, 249);
		}

		label {
            display: none;
		}

		a:link {
			text-decoration: none;
			font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
			font-weight: 700;
		}

        nav {
            display: grid;
            grid-template-areas: 
            'home drawings videos installations performances contact';
            background-color: rgb(255, 252, 249);
            padding: 2em;
        }
		
	}

	@media (width<35em) {
        nav {
            display: none;
        }

		*,
		*:before,
		*:after {
			box-sizing: border-box;
		}

		body {
			font-size: 1.2em;
			line-height: 1.6;
			overflow-x: hidden;
			background-color: rgb(255, 252, 249);
		}

		label .menu {
			position: fixed;
			right: -100px;
			top: -120px;
			z-index: 100;
			width: 200px;
			height: 200px;
			background: #ffffff;
			border-radius: 50% 50% 50% 50%;
			-webkit-transition: 0.5s ease-in-out;
			transition: 0.5s ease-in-out;
			box-shadow: 0 0 0 0 #fff, 0 0 0 0 #fff;
			cursor: pointer;
		}

		label .hamburger {
			position: absolute;
			top: 150px;
			left: 50px;
			width: 30px;
			height: 2px;
			background: #000000;
			display: block;
			-webkit-transform-origin: center;
			transform-origin: center;
			-webkit-transition: 0.5s ease-in-out;
			transition: 0.5s ease-in-out;
		}

		label .hamburger:after,
		label .hamburger:before {
			-webkit-transition: 0.5s ease-in-out;
			transition: 0.5s ease-in-out;
			content: '';
			position: absolute;
			display: block;
			width: 100%;
			height: 100%;
			background: #000000;
		}

		label .hamburger:before {
			top: -10px;
		}

		label .hamburger:after {
			bottom: -10px;
		}

		label input {
			display: none;
		}

		label input:checked + .menu {
			box-shadow: 0 0 0 100vw #fff, 0 0 0 100vh #fff;
			border-radius: 0;
		}

		label input:checked + .menu .hamburger {
			-webkit-transform: rotate(45deg);
			transform: rotate(45deg);
		}

		label input:checked + .menu .hamburger:after {
			-webkit-transform: rotate(90deg);
			transform: rotate(90deg);
			bottom: 0;
		}

		label input:checked + .menu .hamburger:before {
			-webkit-transform: rotate(90deg);
			transform: rotate(90deg);
			top: 0;
		}

		label input:checked + .menu + ul {
			opacity: 1;
		}

		label ul {
			z-index: 200;
			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			opacity: 0;
			transition: 0.25s 0.05s ease-in-out;
			font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		}

		label a {
			margin-bottom: 1em;
			display: block;
			color: #000000;
			text-decoration: none;
		}

		.arrow {
			width: 2em;
			margin-bottom: -20em;
			transform: rotate(180deg);
			margin-left: 1em;
		}
	}

</style>
