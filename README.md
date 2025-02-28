# 📌 Déclaration des Variables en JavaScript

En JavaScript, on utilise trois mots-clés principaux pour déclarer des variables : `var`, `let` et `const`.

## 1️⃣ `var` (Obsolète, à éviter 🚫)
- Déclaration **ancienne** (avant ES6).
- Portée **fonctionnelle** (accessible dans toute la fonction où elle est déclarée).
- **Hoisting** : Les variables `var` sont remontées en haut du scope, mais sans leur valeur initiale.

### Exemple :
```js
console.log(x); // undefined (mais pas d'erreur)
var x = 10;
```

⚠️ **Problèmes avec `var`** :
- Peut être redéclarée dans le même scope.
- Peut provoquer des comportements inattendus à cause du hoisting.

---

## 2️⃣ `let` (Recommandé ✅)
- Introduit avec **ES6** (2015).
- Portée **bloc** (`{}`), ce qui réduit les erreurs.
- Ne peut pas être redéclarée dans le même scope.

### Exemple :
```js
let y = 20;
y = 30; // ✅ Possible (modifiable)
console.log(y); // 30

{
    let y = 50; // Scope différent
    console.log(y); // 50
}
console.log(y); // 30
```

---

## 3️⃣ `const` (Valeur constante 🔒)
- Portée **bloc** (`{}`).
- **Ne peut pas être réassignée** après l'initialisation.
- Obligatoire d'initialiser une valeur lors de la déclaration.

### Exemple :
```js
const z = 40;
z = 50; // ❌ Erreur ! Impossible de modifier une constante.
```

🔹 **Cas des objets et tableaux avec `const`**  
Les objets et tableaux déclarés avec `const` **peuvent être modifiés**, mais **pas réassignés**.

```js
const person = { name: "Ali" };
person.name = "Omar"; // ✅ Possible
// person = { name: "Mehdi" }; ❌ Erreur !
```

---

## 🔥 Bonnes Pratiques
✔️ **Utiliser `const` par défaut**.  
✔️ Utiliser `let` si la variable doit changer.  
✔️ **Éviter `var`** pour éviter les erreurs liées au hoisting.

---

📌 **Auteur :** Imani Mourad  
🚀 *N'hésitez pas à contribuer ou à poser des questions !*

# basics_js
