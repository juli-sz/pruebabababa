<script>
    // Ejemplo de datos para las cards
    import Carrusel from "../../components/Carrusel.svelte";

    let cards = [
        { id: 1, title: 'Card 1', escultorPantalla:'obra1', escultorObras: 'https://tecdn.b-cdn.net/img/new/standard/nature/186.jpg', content: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.', escultorName:'Pablo Picasso', escultorPais:'src/public/arg.png', escultorFoto:'src/public/pablopicasso.png'},
        { id: 2, title: 'Card 2', escultorPantalla:'obra2', escultorObras: 'https://tecdn.b-cdn.net/img/new/standard/nature/186.jpg', content: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.', escultorName:'Pablo Picasso', escultorPais:'src/public/arg.png', escultorFoto:'src/public/pablopicasso.png'},
        { id: 3, title: 'Card 3', escultorPantalla:'obra3', escultorObras: 'https://tecdn.b-cdn.net/img/new/standard/nature/186.jpg', content: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.', escultorName:'Pablo Picasso', escultorPais:'src/public/arg.png', escultorFoto:'src/public/pablopicasso.png'},
        { id: 4, title: 'Card 4', escultorPantalla:'obra4', escultorObras: 'https://tecdn.b-cdn.net/img/new/standard/nature/186.jpg', content: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.', escultorName:'Pablo Picasso', escultorPais:'src/public/arg.png', escultorFoto:'src/public/pablopicasso.png'},
        { id: 5, title: 'Card 5', escultorPantalla:'obra5', escultorObras: 'https://tecdn.b-cdn.net/img/new/standard/nature/186.jpg', content: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.', escultorName:'Pablo Picasso', escultorPais:'src/public/arg.png', escultorFoto:'src/public/pablopicasso.png'},
        { id: 6, title: 'Card 6', escultorPantalla:'obra6', escultorObras: 'https://tecdn.b-cdn.net/img/new/standard/nature/186.jpg', content: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.', escultorName:'Pablo Picasso', escultorPais:'src/public/arg.png', escultorFoto:'src/public/pablopicasso.png'}
        // Añade más cards si es necesario
    ];
</script>

<!-- Contenedor de las cards -->
<div class="grid gap-4 grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 p-4">
    {#each cards as card}
        <div class="block rounded-lg bg-white shadow-secondary-1 m-2.5 border-2 border-gray-300 rounded-md">
            <div class="relative overflow-hidden bg-cover bg-no-repeat">
                <Carrusel/>
                <a href={card.escultorPantalla}>
                    <img
                            src={card.escultorFoto}
                            class="w-32 rounded-full"
                            alt="Avatar" />
                    <div class="absolute bottom-0 left-0 right-0 top-0 h-full w-full overflow-hidden bg-[hsla(0,0%,98%,0.15)] bg-fixed opacity-0 transition duration-300 ease-in-out hover:opacity-100"></div>
                </a>
            </div>
            <div class="p-6 text-surface dark:text-white">
                <h5 class="mb-2 text-xl font-medium leading-tight text-black">{card.escultorName}  <img class="max-h-5" src={card.escultorPais} /> </h5>
                <p class="mb-4 text-base text-left text-black">{card.content}</p>
            </div>
        </div>
    {/each}
</div>


