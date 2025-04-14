# partageIntraAttaque
```BASH
function formatDateToDDMMYYYY(isoDateString) {
    // Créer un objet Date à partir de la chaîne ISO
    const date = new Date(isoDateString);

    // Extraire le jour, le mois et l'année
    const day = String(date.getDate()).padStart(2, '0'); // Ajoute un zéro en tête si nécessaire
    const month = String(date.getMonth() + 1).padStart(2, '0'); // Les mois sont indexés à partir de 0
    const year = date.getFullYear();

    // Retourner la date formatée
    return `${day}/${month}/${year}`;
}
```
