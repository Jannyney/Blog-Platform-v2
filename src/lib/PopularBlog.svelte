<script lang="ts">
    import {returnBlog} from "./blog";
    let projects = ["one", "two", "three", "four", "five", "six"]
</script>


<div class="flex flex-col items-center " id="project">
    <p class="text-5xl font-bold p-20">Top Blogs</p>
    <div class="flex flex-col md:flex-row flex-wrap items-center md:justify-center">

        {#each projects as project }
        <div class="card card-compact w-96 bg-base-100 shadow-xl mx-20 my-10">
          <figure><img src="{returnBlog(project)?.post.image}" alt="BlogImg" /></figure>
          <div class="card-body">
            <h2 class="card-title">{returnBlog(project)?.post.title}</h2>
           <div class="card-actions justify-end">
              <a href="/blog/{project}" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
    {/each}
    </div>
</div>