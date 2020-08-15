<template>
    <div>
        <div class="bg-white mb-16">
            <div class="container py-10 pb-16">
                <div class="w-10/12">
                    <input
                        class="text-4xl text-gray-700 font-medium font-header leading-tight mb-4 w-full p-2 border-2 rounde d border-dashed border-gray-400"
                        value=""
                        placeholder="Untitled snippet"
                    />

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
            <div class="flex items-center mb-6">
                <div class="text-xl text-gray-600 font-medium mr-3">
                    1/1
                </div>
                <input
                    id=""
                    type="text"
                    name=""
                    class="text-xl text-gray-600 font-medium p-2 py-1 border-2 rounded border-dashed border-gray-400 bg-transparent"
                    value=""
                    placeholder="Untitled step"
                />
            </div>

            <div class="flex flex-wrap lg:flex-no-wrap">
                <div
                    class="w-full lg:w-8/12 lg:mr-16 flex flex-wrap lg:flex-no-wrap justify-between items-start"
                >
                    <div class="flex flex-row lg:flex-col order-first mr-2">
                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg mr-2 lg:mr-0"
                            title="Next Step"
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

                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg mr-2 lg:mr-0"
                            title="Add Step Before"
                        >
                            <svg
                                class="h-6 text-white"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </nuxt-link>
                    </div>
                    <div class="w-full mb-8">
                        <textarea
                            class="w-full border-dashed border-2 border-gray-400 rounded-lg"
                        >
Editor
                        </textarea>
                        <div class="bg-white p-8 rounded-lg text-gray-600">
                            Markdown content
                        </div>
                    </div>

                    <div
                        class="flex flex-row lg:flex-col order-first lg:order-last"
                    >
                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg ml-2"
                            title="Previous Step"
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
                            title="Add Step After"
                        >
                            <svg
                                class="h-6 text-white"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </nuxt-link>

                        <nuxt-link
                            :to="{}"
                            class="block mb-4 p-3 bg-blue-500 rounded-lg ml-2"
                            title="Delete step"
                        >
                            <svg
                                class="h-6 text-white"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z"
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
