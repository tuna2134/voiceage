<script lang="ts">
    import items from "./items.json";
    import Head from "../lib/head.svelte";
</script>

<Head title="一覧" description="VOICEVOXの利用例がここに載っています。" />
<div class="w-full max-w-6xl mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-3">
        {#each items as item}
        <div class="mx-2 bg-white px-2 py-2 rounded">
            <div class="flex justify-center my-1.5">
                <img class="w-48 h-48 flex justify-center" src={item.logo} alt="logo" />
            </div>
            <div class="my-1.5">
                <p class="text-3xl text-center font-semibold">{item.name}</p>
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