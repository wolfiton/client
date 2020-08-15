<template>
    <div>
        <div class="bg-white mb-16">
            <div class="container py-10 pb-16">
                <div class="w-10/12">
                    <h1
                        class="text-4xl text-gray-700 font-medium leading-tight mb-4"
                    >
                        Snippet title
                    </h1>
                    <div class="text-gray-600">
                        Created by:

                        <nuxt-link :to="{}">
                            Wolf
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <h1 class="text-xl text-gray-600 font-medium mb-6">
                1/1 Step title
            </h1>
            <div class="flex flex-wrap lg:flex-no-wrap">
                <div
                    class="w-full lg:w-8/12 lg:mr-16 flex flex-wrap lg:flex-no-wrap justify-between items-start"
                >
                    <div class="order-first">
                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg mr-2"
                        >
                            <svg
                                class="h-6 text-white"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M9.707 16.707a1 1 0 01-1.414 0l-6-6a1 1 0 010-1.414l6-6a1 1 0 011.414 1.414L5.414 9H17a1 1 0 110 2H5.414l4.293 4.293a1 1 0 010 1.414z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </nuxt-link>
                    </div>

                    <div
                        class="bg-white p-8 rounded-lg text-gray-600 w-full mb-8"
                    >
                        Markdown column for snippets
                    </div>

                    <div
                        class="flex flex-row lg:flex-col order-first lg:order-last"
                    >
                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg ml-2"
                        >
                            <svg
                                class="h-6 text-white"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </nuxt-link>

                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg ml-2"
                            title="Edit step"
                        >
                            <svg
                                class="h-6 text-white"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    d="M17.414 2.586a2 2 0 00-2.828 0L7 10.172V13h2.828l7.586-7.586a2 2 0 000-2.828z"
                                />
                                <path
                                    fill-rule="evenodd"
                                    d="M2 6a2 2 0 012-2h4a1 1 0 010 2H4v10h10v-4a1 1 0 112 0v4a2 2 0 01-2 2H4a2 2 0 01-2-2V6z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </nuxt-link>
                    </div>
                </div>
                <div class="w-full lg:w-4/12">
                    <div class="mb-8">
                        <h1 class="text-xl text-gray-600 font-medium mb-6">
                            Steps
                        </h1>

                        <ul>
                            <li
                                v-for="(step, index) in 5"
                                :key="index"
                                class="mb-1"
                            >
                                <nuxt-link
                                    :to="{}"
                                    :class="{ 'font-bold': index === 0 }"
                                >
                                    {{ index + 1 }}. Step title
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                    <div class="text-gray-500 text-sm">
                        Use
                        <div
                            class="inline-block font-semibold leading-relaxed text-sm text-gray-600 bg-gray-400 p-2"
                        >
                            CTRL
                        </div>
                        +
                        <div
                            class="inline-block font-semibold leading-relaxed text-sm text-gray-600 bg-gray-400 p-2"
                        >
                            SHIFT
                        </div>
                        +
                        <div
                            class="inline-block font-semibold leading-relaxed text-sm text-gray-600 bg-gray-400 p-2"
                        >
                            LEFT OR RIGHT
                        </div>
                        ARROWS ON YOUR KEYBOARD TO NAVIGATE BETWEEN STEPS
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
