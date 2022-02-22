<template>
    <div>
        <nav class="navbar navbar-dark bg-dark sticky-top">
            <ul class="navbar-nav flex-row">
                <li class="nav-item mr-3">
                    <nuxt-link class="nav-link" to="/"> Accueil </nuxt-link>
                </li>
                <li class="nav-item">
                    <nuxt-link class="nav-link" to="/commandes">
                        Commandes
                    </nuxt-link>
                </li>
            </ul>
        </nav>
        <div
            class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0"
        >
            <link
                href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
                rel="stylesheet"
            />
            <Nuxt />
        </div>
    </div>
</template>

<script>
export default {
    name: "DefaultLayout",
};
</script>
