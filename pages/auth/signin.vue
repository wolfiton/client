<template>
    <div class="container mt-16">
        <div class="flex flex-col items-center">
            <h2 class="text-3xl text-gray-700 font-medium mb-10">
                Hello
            </h2>
            {{ validations }}
            <form
                action="#"
                class="bg-white p-8 rounded w-full md:w-6/12 lg:w-4/12 mb-6"
                @submit.prevent
            >
                <div class="mb-6">
                    <label
                        for="email"
                        class="block text-gray-600 font-medium mb-2"
                        :class="{ 'text-red-500': validations.email }"
                    >
                        Email
                    </label>

                    <input
                        id="email"
                        v-model="form.email"
                        type="text"
                        placeholder="Email"
                        name="email"
                        class="block w-full p-3 border-2 border-gray-400 rounded"
                        :class="{ 'border-red-500': validations.email }"
                    />
                    <div
                        v-if="validations.email"
                        class="flex items-center justify-end"
                    >
                        <p
                            class="text-gray-200 bg-red-700 px-4 py-2 font-medium rounded"
                        >
                            {{ validations.email[0] }}
                        </p>
                    </div>
                </div>
                <div class="mb-6">
                    <label
                        for="password"
                        class="block text-gray-600 font-medium mb-2"
                        :class="{ 'text-red-500': validations.password }"
                    >
                        Password
                    </label>

                    <input
                        id="password"
                        v-model="form.password"
                        type="password"
                        placeholder="Password"
                        name="password"
                        class="block w-full p-3 border-2 border-gray-400 rounded"
                        :class="{ 'border-red-500': validations.password }"
                    />
                    <div
                        v-if="validations.password"
                        class="flex items-center justify-end"
                    >
                        <p
                            class="text-gray-200 bg-red-700 px-4 py-2 font-medium rounded"
                        >
                            {{ validations.password[0] }}
                        </p>
                    </div>
                </div>

                <button
                    class="px-4 py-2 bg-blue-700 text-gray-200 hover:bg-blue-600 block w-full font-medium text-xl"
                    @click="submit"
                >
                    Sign In
                </button>
            </form>
            <div class="text-center text-gray-600">
                No account?
                <nuxt-link :to="{ name: 'index' }">Create one here</nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                email: '',
                password: '',
            },

            validations: {},
        }
    },
    methods: {
        async submit() {
            try {
                await this.$auth.loginWith('local', {
                    data: this.form,
                })
            } catch (e) {
                if (e.response.status === 422) {
                    this.validations = e.response.data.errors
                }
            }
        },
    },
    head() {
        return { title: 'Sign In' }
    },
}
</script>

<style scoped></style>
