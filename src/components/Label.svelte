<script>
import {annotate} from 'svelte-rough-notation';  
export let tech;
</script>

<span use:annotate={{ visible: true, type: 'highlight', color: '#FAD7A0', iterations: 2}}>
    {tech}
</span>

<style>
    span {
        padding: 0em 0.1em;
        margin: 0em 0.2em;
        color: var(--dark);
    }
</style>