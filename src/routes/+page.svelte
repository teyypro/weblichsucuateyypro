<script>
    import MainBoard from "../components/TimeLine/MainBoard.svelte";
    import Gallery from "../components/ViewSphere/Gallery.svelte";
    import { change } from '../store.js'
</script>
{#if $change == '0'}
<MainBoard/>
{:else}
<Gallery/>
{/if}