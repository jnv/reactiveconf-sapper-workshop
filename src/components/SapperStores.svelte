<script>
  import {onMount} from 'svelte';
  import {stores} from '@sapper/app';
  const {page, preloading, session} = stores();
  page.subscribe(args => {
    console.log('page.subscribe', args);
  });
</script>
