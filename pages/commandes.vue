<template>
    <div>
        <titre-page :titre="titre" />
        <div class="absolute top-1/4 left-0 w-screen">
            <h2 class="mx-6 mb-6 h2">Produits disponibles</h2>
            <div class="card-deck mx-6">
                <Produit
                    v-for="produit in produits"
                    :key="produit.nom"
                    :nom="produit.nom"
                    :prix="produit.prix"
                    role="commander"
                    @commande="ajouterProduit"
                />
            </div>
            <h2 class="m-6 h2">Produits commandés</h2>
            <div class="card-deck mx-6">
                <Produit
                    v-for="produit in commandes"
                    :key="produit.nom"
                    :nom="produit.nom"
                    role="affichage"
                    :prix="produit.prix"
                />
            </div>
        </div>
    </div>
</template>

<script>
import titrePage from "@/components/titrePage.vue";
import Produit from "~/components/Produit.vue";

export default {
    name: "Commandes",
    components: {
        titrePage,
        Produit,
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
            commandes: [{ nom: "Frites", prix: 2.0 }],
        };
    },
    methods: {
        ajouterProduit(nom, prix) {
            this.commandes.push({ nom: nom, prix: prix });
        },
    },
};
</script>

<style scoped></style>
