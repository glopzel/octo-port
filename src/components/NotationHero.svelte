<script>
    import {Annotation, annotate} from 'svelte-rough-notation';
    import { onMount } from 'svelte';

    let rn;
  let visible = false;
  let actionsVisible = false;

  onMount(() => {
    setTimeout(() => {
      visible = true;
      actionsVisible = true;
    }, 1000);
  });
</script>

<h1 class="hero-heading">
    <Annotation bind:visible bind:this={rn} type="box" padding={10}>
        Hello, I'm <span class="hero-heading" use:annotate={{ visible: actionsVisible, color: '#ff8906', type: 'highlight' }}>Angela</span>
        <span class="hero-heading" use:annotate={{ visible: actionsVisible, color: '#ff8906', type: 'highlight' }}>Lopez</span>, software developer based somewhere in Chile
    </Annotation>
</h1>
