<template>
    <div class="flex items-center bg-white py-8 lg:py-0">
        <div class="flex flex-wrap items-center container lg:flex-no-wrap">
            <nuxt-link :to="{ name: 'index' }" class="mr-10 flex-shrink-0">
                <img src="~/assets/logo.svg" alt="Logo" class="h-8" />
            </nuxt-link>
            <a
                href="#"
                class="lg:hidden flex flex-col relative justify-center w-8 h-8 ml-auto"
                @click.prevent="mobileNavOpen = !mobileNavOpen"
            >
                <span
                    class="bg-blue-500 h-1 w-8 rounded mb-1"
                    :class="{
                        'absolute right-0 origin-center transform -rotate-45': mobileNavOpen,
                    }"
                >
                </span>
                <span
                    class="bg-blue-500 h-1 w-8 rounded mb-1"
                    :class="{
                        'absolute right-0 origin-center transform rotate-45': mobileNavOpen,
                    }"
                >
                </span>
                <span
                    class="bg-blue-500 h-1 w-8 rounded mb-1"
                    :class="{
                        'hidden mr-1': mobileNavOpen,
                    }"
                >
                </span>
            </a>
            <div
                class="flex w-full"
                :class="{
                    'mt-8': mobileNavOpen,
                    'hidden lg:flex': !mobileNavOpen,
                }"
            >
                <ul class="lg:flex items-center w-full lg:w-auto lg:h-24">
                    <li>
                        <nuxt-link
                            :to="{ name: 'index' }"
                            class="text-lg text-gray-700 lg:px-4 lg:py-8"
                        >
                            Browse
                        </nuxt-link>
                    </li>
                    <li>
                        <nuxt-link
                            :to="{ name: 'index' }"
                            class="text-lg text-gray-700 lg:px-4 lg:py-8"
                        >
                            Search
                        </nuxt-link>
                    </li>
                </ul>

                <ul
                    class="lg:flex items-center w-full lg:w-auto lg:h-24 ml-auto text-right"
                >
                    <template v-if="$auth.loggedIn">
                        <li>
                            <nuxt-link
                                :to="{ name: 'dashboard' }"
                                class="text-lg text-gray-700 lg:px-4 lg:py-8"
                            >
                                Dashboard
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link
                                :to="{ name: 'index' }"
                                class="text-lg text-gray-700 lg:px-4 lg:py-8"
                            >
                                {{ $auth.user.name }}
                            </nuxt-link>
                        </li>

                        <li>
                            <a
                                href="#"
                                class="text-lg text-gray-700 lg:px-4 lg:py-8"
                                @click.prevent="signOut()"
                            >
                                Sign out
                            </a>
                        </li>
                    </template>
                    <template v-else>
                        <li>
                            <nuxt-link
                                :to="{ name: 'auth-signin' }"
                                class="text-lg text-gray-700 lg:px-4 lg:py-8"
                            >
                                Sign in
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link
                                :to="{ name: 'index' }"
                                class="text-lg text-gray-700 lg:px-4 lg:py-8"
                            >
                                Create an account
                            </nuxt-link>
                        </li>
                    </template>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            mobileNavOpen: false,
        }
    },
    methods: {
        async signOut() {
            await this.$auth.logout()
        },
    },
}
</script>

<style lang="scss" scoped></style>
