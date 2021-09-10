<template>
	<div class="app">
		<Header title="The Anime Quoter" />
		<Quote />
	</div>
</template>

<script>
import Header from "./components/Header.vue";
import Quote from "./components/Quote.vue";

export default {
    name: 'App',
    components: { 
		Header,
		Quote
	}
}
</script>


<style lang="scss">
:root {
	--primary: #D81E5B;
	--secondary: #8a4fff;
	--tertiary: #32cbff;
	--dark: #131a26;
	--light: #EEE;
	--grey: #848484;
}

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-family: "Fire Sans", sans-serif;
}

 


</style>
