<template>
    <div class="card text-white bg-dark mb-3 w-auto">
        <div class="card-header">{{ nom }}</div>
        <div class="card-body">
            <p class="card-text">{{ prix }} €</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "Produit",
    props: ["nom", "prix"],
};
</script>
