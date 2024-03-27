<script>
   // this is declare properties
   export let addPost;

   let author = '';
   let post = '';

   function sendPost() {
     addPost(author, post);
     author = '';
     post = '';
   }
</script>

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
   
   <button on:click={sendPost} class="btn btn-primary">Submit</button>
</div>
