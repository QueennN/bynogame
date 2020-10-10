<template>
    <div
        class="w-full max-w-sm overflow-hidden rounded-lg border bg-white shadow m-5"
    >
        <div class="relative">
            <img
                class="h-48 w-full bg-cover bg-no-repeat bg-center object-cover transition transform  duration-500 hover:-translate-y-1 hover:scale-110"
                :src="_download"
            />
            <div
                style="background-color: rgba(0,0,0,0.6)"
                class="absolute bottom-0 mb-2 ml-3 px-2 py-1 rounded text-sm text-white"
            >
                {{ _id }}
            </div>
        </div>
        <div class="p-3">
            <h3 class="mr-10 text-sm truncate-2nd">
                {{ _author }}
            </h3>
            <div class="flex items-start justify-between">
                <p class="text-xs text-gray-500">Download Url</p>
                <button
                    class="outline text-xs text-gray-500 hover:text-blue-500"
                    title="Bookmark this ad"
                >
                    <i class="far fa-bookmark"></i>
                </button>
                <p class="text-xs text-gray-500">
                    <a
                        :href="_image"
                        class="hover:underline hover:text-blue-500"
                        >Click to download</a
                    >
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ["_id", "_text", "_author", "_image", "_download"]
};
</script>

<style>
</style>