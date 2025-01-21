<script lang="ts" setup>
import { reactive, ref } from 'vue';
import type { Student } from '@/models/student';
const student = reactive<Student>({
    nom: '',
    prenom: '',
    email: '',
    sexe: '',
    adresse: '',
    codePostal: '',
    ville: '',
    institut: '',
})
const formErrors = reactive({
    nom: '',
    prenom: '',
    email: '',
    sexe: '',
    adresse: '',
    codePostal: '',
    ville: '',
    institut: '',
})
const displayEntries = ref(false);
const validateForm = () => {
    formErrors.nom = '';
    formErrors.prenom = '';
    formErrors.email = '';
    formErrors.sexe = '';
    formErrors.adresse = '';
    formErrors.codePostal = '';
    formErrors.ville = '';
    formErrors.institut = '';
    let erreur = false;
    if (!student.nom) {
        formErrors.nom = "Erreur : Il faut remplir le champ de nom"
        erreur = true;
    }
    if (!student.prenom) {
        formErrors.prenom = "Erreur : Il faut remplir le champ de prénom"
        erreur = true;
    }
    if (!student.email) {
        formErrors.email = "Erreur : Il faut remplir le champ de email"
        erreur = true;
    }
    if (!student.sexe) {
        formErrors.nom = "Erreur : Il faut remplir le champ de sexe"
        erreur = true;
    }
    if (!student.adresse) {
        formErrors.adresse = "Erreur : Il faut remplir le champ de adresse"
        erreur = true;
    }
    if (!student.codePostal) {
        formErrors.codePostal = "Erreur : Il faut remplir le champ de Code Postal"
        erreur = true;
    }
    if (!student.ville) {
        formErrors.ville = "Erreur : Il faut remplir le champ de ville"
        erreur = true;
    }
    if (!student.institut) {
        formErrors.institut = "Erreur : Il faut remplir le champ de nom de l'institut"
        erreur = true;
    }
    if (!erreur) {
        displayEntries.value = true;
    }
}
</script>
<template>
    <h1>Formulaire d'inscription</h1>
    <h2 v-for="(error) in formErrors">{{ error }}</h2>
    <form @submit.prevent="validateForm">
        <label for="nom">Nom</label>
        <input v-model="student.nom" id="nom">
        <label for="prenom"> Prénom</label>
        <input v-model="student.prenom" id="prenom">
        <br/>
        <label for="email">Email</label>
        <input v-model="student.email" id="email">
        <br/>
        <label for="homme">Sexe : Homme</label>
        <input type="radio" v-model="student.sexe" id="homme" value="Homme" name="sexe">
        <label for="femme"> Femme</label>
        <input type="radio" v-model="student.sexe" id="femme" value="Femme" name="sexe">
        <br/>
        <label for="adresse">Adresse</label>
        <input v-model="student.adresse" id="adresse">
        <br/>
        <label for="codePostal">Code Postal</label>
        <input v-model="student.codePostal" id="codePostal">
        <label for="ville">Ville</label>
        <input v-model="student.ville" id="ville">
        <br/>
        <label for="institut">Nom de l'institut</label>
        <input v-model="student.institut" id="institut">
        <br/>
        <button type="submit">Valider</button>
        <button type="reset">Annuler</button>
    </form>
    <h2 v-if="displayEntries" v-for="(element) in student">{{ element }}</h2>
</template>
<style></style>