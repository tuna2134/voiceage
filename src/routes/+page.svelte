<script lang="ts">
    import items from "./items.json";
    import Head from "../lib/head.svelte";
</script>

<Head title="一覧" description="VOICEVOXの利用例がここに載っています。" />
<div class="h-36 bg-white flex items-center">
    <div class="w-full mx-auto">
        <h2 class="text-center text-3xl font-semibold">利用例</h2>
        <p class="text-center text-gray-400">ここにはVOICEVOXを利用したYouTubeチャンネルやDiscordボットなどがあります。</p>
    </div>
</div>
<div class="bg-[#e3ffe8] min-h-screen py-4">
    <div class="w-full max-w-6xl mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-3">
            {#each items as item}
            <div class="mx-2 bg-white px-2 py-2 rounded">
                <div class="flex justify-center my-1.5">
                    <img class="w-48 h-48 flex justify-center" src={item.logo} alt="logo" />
                </div>
                <div class="my-1.5">
                    <a href={item.url} class="hover:text-[#A5D4AD]">
                        <p class="text-2xl text-center font-semibold">{item.name}</p>
                    </a>
                </div>
                <div class="my-1.5 flex justify-center">
                    {#each item.tags as tag}
                    <p class="bg-[#5865F2] text-white rounded-xl px-2 py-0.5">{tag}</p>
                    {/each}
                </div>
                <div class="my-1.5">
                    <p class="text-center">{item.description}</p>
                </div>
            </div>
            {/each}
        </div>
    </div>
</div>