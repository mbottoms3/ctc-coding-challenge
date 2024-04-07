<script setup>
import { Link } from "@inertiajs/vue3";
</script>

<template>
    <div>
        <div class="min-h-screen bg-gray-100">
            <nav class="bg-white border-b border-gray-100">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                    <div class="flex justify-end h-16">
                        <div class="flex">
                            <div class="space-x-8 sm:-my-px sm:ms-10 sm:flex">
                                <button>
                                    <Link
                                        method="post"
                                        :href="route('logout')"
                                        class="rounded-md px-3 py-2 text-black"
                                    >
                                        Logout
                                    </Link>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </nav>

            <!-- Page Heading -->
            <header class="bg-white shadow" v-if="$slots.header">
                <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                    <slot name="header" />
                </div>
            </header>

            <!-- Page Content -->
            <main>
                <slot />
            </main>
        </div>
    </div>
</template>
