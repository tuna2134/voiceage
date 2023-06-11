<script>
    import "../app.css";

    let items = {
        headers: [
            {
                name: "追加申請",
                value: "https://forms.gle/i7ovok45NbHev75z8",
            },
            {
                name: "official",
                value: "https://voicevox.hiroshiba.jp/",
            }
        ],
    }
</script>

<div class="flex flex-col min-h-screen">
    <header class="w-full flex border-b">
        <div class="w-full flex items-center max-w-5xl mx-auto h-16 px-2">
            <h1 class="text-2xl flex font-bold">VOICEAGE</h1>
            <nav class="flex ml-auto space-x-4">
                {#each items.headers as item}
                <a href={item.value}>{item.name}</a>
                {/each}
            </nav>
        </div>
    </header>
    <main class="py-4 min-h-screen">
        <slot />
    </main>
    <footer class="mt-auto w-full flex border-t">
        <div class="w-full flex items-center max-w-5xl mx-auto h-24 px-2">
            <p class="flex text-2xl font-bold">VOICEAGE</p>
            <p class="ml-auto">&copy; 2023 tuna2134</p>
        </div>
    </footer>
</div>

<style lang="postcss"></style>