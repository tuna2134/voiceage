<script lang="ts">
    export let title: string;
    export let description: string;
</script>

<head>
    <title>{title} | VOICEAGE</title>
    <meta content={description} name="description" />
    <meta property="og:title" content={`${title} | VOICEAGE`} />
    <meta property="og:description" content={description} />
    <meta property="og:type" content="website" />
    <meta property="og:site_name" content="VOICEAGE" />
    <meta property="og:locale" content="ja_JP"  />
</head>