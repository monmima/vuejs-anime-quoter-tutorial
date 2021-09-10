<template>
	<div class="app">
		<Header title="The Anime Quoter" />
		<Quote :quote="quote" />
		<div class="button-container">
			<button @click="getQuote">Generate</button>
		</div>
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
	},
	data() {
		return {
			// default value
			// quote: {
			// 	content: "Content goes here",
			// 	anime: "Naruto",
			// 	character: "Madara"
			// },

			// default value: empty
			quote: {},

			quotes: []
		}
	},
	methods: {
		async getQuote() {

			// to store the data
			// if (this.quote.content) {
			// 	this.quotes = [...this.quote, this.quote]
			// }

			const data = await fetch("https://animechan.vercel.app/api/random")
				.then (res => res.json());

			this.quote = {
				content: data.quote,
				anime: data.anime,
				character: data.character
			};

		}

	},
	created() {
		// this.getQuote();
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

.button-container {
	display: flex;
	justify-content: center;
	padding: 0 32px;

	margin: 64px auto;

	button {
		border: none;
		outline: none;
		background-color: var(--primary);

		padding: 16px 32px;
		border-radius: 99px;

		color: var(--light);
		font-size: 28px;
		font-weight: 700;
		text-transform: uppercase;
		cursor: pointer;
		transition: 0.4s;

		&:hover {
			background-color: var(--secondary);
		}
	}
}

</style>
