<template>
	<header>
		<h1>{{ title }}</h1>
	</header>
</template>

<script>
export default {
	props: ["title"]
}
</script>

<style lang="scss" scoped>
header {
	display: flex;
	font-size: 1.2rem;
	justify-content: center;
	padding: 24px 32px;

	h1 {
		border-bottom: 5px solid var(--primary);
		color: var(--dark);
		font-size: 32px;
		font-weight: 700;
		padding-bottom: 8px;
		text-align: center;
		text-transform: uppercase;
	}
}


</style>