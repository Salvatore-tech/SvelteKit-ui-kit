<script lang="ts">

    export let preTitle: string;
    export let title: string;
    export let description: string;
    export let author: string;
    export let variantFilling: string = '';
    export let imgLink = '';
</script>


<div class="text-token grid grid-cols-1 gap-4 m-4">

    <a class="card card-hover overflow-hidden {variantFilling}" href="/elements/cards">
        {#if imgLink}
            <header>
                <img src={imgLink} class="bg-black/50 w-full aspect-[21/9]" alt="Post"
                     style="max-height:200px; object-fit:cover"/>
            </header>

        {/if}
        <div class="p-4 space-y-4">
            <h6 class="font-light text-sm md:text-base lg:text-lg" data-toc-ignore>{preTitle}</h6>
            <h3 class="font-semibold text-md md:text-lg lg:text-xl" data-toc-ignore>{title}</h3>
            <article>
                <p class="text-sm md:text-base lg:text-lg">
                    <!-- cspell:disable -->
                    {description}
                    <!-- cspell:enable -->
                </p>
            </article>
        </div>
        <hr class="opacity-50"/>
        <footer class="p-4 flex justify-start items-center space-x-4">
            <div class="flex-auto flex justify-between items-center">
                <h6 class="font-medium text-sm md:text-base lg:text-lg" data-toc-ignore>{author}</h6>
                <small class="font-light">On {new Date().toLocaleDateString("it")}</small>
            </div>
        </footer>
    </a>
</div>