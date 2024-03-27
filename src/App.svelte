<script>
  import data from './data.json';
  import Post from './components/Post.svelte';
  import Form from './components/Form.svelte';

  let posts = data.data

  function addPost(author, post) {
    const _post = {
      id: posts.length + 1,
      author: author,
      post: post
    }
    posts.push(_post)
    posts = posts;//redeclare the posts to trigger the reactivity
  }
</script>

<main class="flex flex-col justify-center items-center space-y-4">
  <Form addPost={addPost} />
  <div class="flex flex-col gap-4">
    {#each posts.reverse() as post }
    <Post {...post} />
    {/each}
  </div>
</main>

<style>

</style>
