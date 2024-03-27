<script>
  import data from './data.json';

  let author = '';
  let post = '';

  let posts = data.data

  function addPost() {
    const _post = {
      id: posts.length + 1,
      author,
      post
    }
    posts.push(_post)
    posts = posts;//redeclare the posts to trigger the reactivity

    author = '';
    post = '';
  }
</script>

<main class="flex flex-col justify-center items-center space-y-4">
  <div class="flex flex-col gap-6">
    <h1>Add Post</h1>
    <label for="author" class="form-control w-full max-w-xs">
      <div class="label">
        <span class="label-text">Author</span>
      </div>
      <input bind:value={author} name="author" type="text" placeholder="Type here" class="input input-bordered w-full max-w-xs" />
    </label>
  
    <label for="post" class="form-control">
      <div class="label">
        <span class="label-text">Post</span>
      </div>
      <textarea bind:value={post} name="post" class="textarea textarea-bordered h-24" placeholder="Write some text"></textarea>
    </label>
    
    <button on:click={addPost} class="btn btn-primary">Submit</button>
  </div>

  <div class="flex flex-col gap-4">
    {#each posts.reverse() as post }
    <div class="card w-96 bg-base-100 shadow-xl">
      <div class="card-body text-left">
        <h2 class="card-title">{post.author}</h2>
        <p>{post.post}</p>
      </div>
    </div>
    {/each}
  </div>
</main>

<style>

</style>
