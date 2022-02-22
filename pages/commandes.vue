<template>
    <div>
        <titre-page :titre="titre" />
        <div class="absolute top-1/4 left-0 w-screen">
            <h2 class="mx-6 mb-6 h2">Produits disponibles</h2>
            <div class="card-deck mx-6">
                <div
                    v-for="produit in produits"
                    :key="produit.nom"
                    class="card text-white bg-dark mb-3 w-auto"
                >
                    <div class="card-header">{{ produit.nom }}</div>
                    <div class="card-body">
                        <p class="card-text">{{ produit.prix }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import titrePage from "@/components/titrePage.vue";
export default {
    name: "Commandes",
    components: {
        titrePage,
    },
    data() {
        return {
            titre: "Commander",
            produits: [
                { nom: "Pizza", prix: 3.0 },
                { nom: "Frites", prix: 2.0 },
                { nom: "Hamburger", prix: 2.5 },
                { nom: "Cheeseburger", prix: 3.0 },
            ],
        };
    },
};
</script>

<style scoped></style>
