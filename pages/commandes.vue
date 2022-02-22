<template>
    <div>
        <titre-page :titre="titre" />
        <div class="container">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus,
            alias aliquam repellat at obcaecati, ipsa suscipit dolore laudantium
            delectus, necessitatibus accusamus similique fugit distinctio
            adipisci rem ipsam quibusdam cum aliquid.
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
        };
    },
};
</script>

<style scoped></style>
