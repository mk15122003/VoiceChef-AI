<script>
  export let url;
  export let id;
</script>

<img
  class="image"
  src={url}
  alt={id ? id.replace(/_/g, ' ') : 'Visual content'}
  loading="lazy"
  decoding="async"
/>

<style lang="scss">
  .image {
    width: 100%;
    object-fit: contain;
  }
</style>
