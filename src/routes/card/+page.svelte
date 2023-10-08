<script lang="ts">
    import CardComponent from '../../components/CardComponent.svelte';


    const preTitle = 'New';
    const title = 'New card component!'
    const description = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet eligendi cumque consequatur tempore sint nisi sapiente. Iste beatae laboriosam iure molestias cum expedita architecto itaque quae rem.'
    const author = 'By Salvatore'
    const variantFilling = 'variant-filled-surface';
    const imgLink1 = 'static/cardsImg/daniel-cheung.jpg'
    const imgLink2 = 'static/cardsImg/musa-ortac.jpg'
    const imgLink3 = 'static/cardsImg/priscilla-du-preez.jpg'
    const imgLink4 = 'static/cardsImg/jessica-knowlden.jpg'
</script>

<div class="cardContainer">
    <CardComponent {preTitle} {title} {description} {author} {variantFilling} imgLink={imgLink1}/>
    <CardComponent {preTitle} {title} {description} {author} {variantFilling} imgLink={imgLink2}/>
    <CardComponent {preTitle} {title} {description} {author} {variantFilling} imgLink={imgLink3}/>
    <CardComponent {preTitle} {title} {description} {author} {variantFilling} imgLink={imgLink4}/>
</div>


<style>
    .cardContainer{
        display: grid; /* start with mobile layout */
        grid-column-gap: 10px; /* space between columns, change as needed */
        grid-row-gap: 10px; /* space between rows, change as needed */
    }

    /* tablet, iPad, lo-res laptops ands desktops */
    @media (min-width:768px)  {
        .cardContainer {
            grid-template-columns: repeat(2, 1fr);
        }  }

    /* big landscape tablets, laptops, and desktops */
    @media (min-width:1025px) {
        .cardContainer {
            grid-template-columns: repeat(3, 1fr);
        }
    }
</style>