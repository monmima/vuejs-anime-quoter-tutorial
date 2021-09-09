<template>
    <section class="quote">
        <div class="quote-content">
            Content goes here...
        </div>
        <div class="quote-info">
            <div class="quote-anime">
                Life
            </div>
            <div class="quote-author">
                Me
            </div>
        </div>
    </section>
</template>

<script>
export default {
    props: ["quote"]
}
</script>


<style lang="scss" scoped>
.quote {
	position: relative;
	padding: 32px;
	margin: 0 auto;
	max-width: 720px;

    &-content {
        position: relative;
        font-size: 28px;
        font-weight: 600;
        background-color: var(--dark);
        color: var(--light);
        padding: 48px 32px;
        border-radius: 16px;
    }

    &-info {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        padding: 32px;
        
        .quote-author, .quote-anime {
            position: absolute;
            padding: 12px 24px;
            font-size: 24px;
            font-weight: 700;
            border-radius: 99px;
            color: var(--light);
            text-align: center;
        }

        .quote-author {
            top: calc(100% -32px);
            right: 0;
            transform: translated(-50%);
            background-color: var(--secondary);
        }
    }
}
</style>