<script>
</script>

<body>
	<footer>
		<a href="" class="home">Home</a>
		<h3 class="email">Email</h3>
		<h3 class="facebook">Facebook</h3>
		<h3 class="telefoon">Telefoon</h3>
	</footer>
</body>

<style>

    a {
        text-decoration: none;
    }

	footer {
		display: grid;
			grid-template-areas: 
            'home email'
            'facebook telefoon';
			background-color: rgb(255, 246, 234);
	}

	@media (width>35em) {
		footer {
			display: grid;
			grid-template-areas: 'home email facebook telefoon';
		}
	}
</style>
