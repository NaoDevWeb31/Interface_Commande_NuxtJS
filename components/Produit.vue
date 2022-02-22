<template>
    <div class="card text-white bg-dark mb-3 w-auto">
        <div class="card-header">{{ nom }}</div>
        <div class="card-body">
            <p class="card-text">{{ prix }} €</p>
            <button
                @click="$emit('commande', nom, prix)"
                class="mt-3 block mx-auto btn btn-success"
                v-if="role == 'commander'"
            >
                Commander
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: "Produit",
    props: ["nom", "prix", "role"],
};
</script>
