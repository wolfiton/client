<template>
    <div class="container mt-16">
        <div class="flex justify-between">
            <h1 class="text-xl text-gray-600 font-medium mb-6">
                Your Snippets (1)
            </h1>

            <a href="#" @click.prevent="createSnippet">+ Create a snippet</a>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        async createSnippet() {
            const snippet = await this.$axios.$post('snippets')

            console.log(snippet.data)
        },
    },
}
</script>

<style lang="scss" scoped></style>
