# Leoproto Application

Ce document décrit les étapes pour compiler et lancer les parties back-office et front-office de l'application Leoproto, ainsi que les URL d'accès.

## Prérequis

Assurez-vous d'avoir les éléments suivants installés sur votre système :

*   **Java Development Kit (JDK) 21** : Nécessaire pour le back-office Spring Boot.
*   **Node.js et npm** : Nécessaire pour le front-office Next.js.

## 1. Back-office 

Le back-office est une application Spring Boot basée sur Gradle.

### Compilation / Construction

Pour compiler le back-office et générer le fichier JAR exécutable :

1.  Ouvrez un terminal.
2.  Naviguez vers le répertoire du back-office :
    ```bash
    cd Leoproto/backend
    ```
3.  Exécutez la commande Gradle pour construire le projet :
    ```bash
    ./gradlew build
    ```

4.Cela compilera le code, exécutera les tests et créera un fichier JAR dans le répertoire `backend/build/libs`.

### Lancement de l'application

Pour lancer le back-office en mode développement :

1.  Ouvrez un terminal (si ce n'est pas déjà fait, ouvrez-en un nouveau si vous avez compilé).
2.  Naviguez vers le répertoire du back-office :
    ```bash
    cd Leoproto/backend
    ```
3.  Lancez l'application Spring Boot :
    ```bash
    ./gradlew bootRun
    ```
    
    L'application démarrera et écoutera généralement sur le port `8080`. Vous verrez des logs indiquant le démarrage de Spring Boot.

### URL d'accès au Back-office (API)

Une fois lancé, le back-office expose son API à l'adresse suivante :

*   **API Root:** `http://localhost:8080`

## 2. Front-office (Next.js)

Le front-office est une application Next.js basée sur Node.js et npm (ou Yarn).

### Installation des dépendances

Avant de compiler ou de lancer, vous devez installer les dépendances Node.js :

1.  Ouvrez un terminal.
2.  Naviguez vers le répertoire du front-office :
    ```bash
    cd Leoproto/frontend
    ```
3.  Installez les dépendances :
    ```bash
    npm install
    # Ou si vous utilisez Yarn :
    # yarn install
    ```

### Compilation / Construction

Pour compiler le front-office pour la production :

1.  Ouvrez un terminal.
2.  Naviguez vers le répertoire du front-office :
    ```bash
    cd Leoproto/frontend
    ```
3.  Exécutez la commande de construction :
    ```bash
    npm run build
    ```
    Cela générera les fichiers optimisés pour la production dans le répertoire `.next`.

### Lancement de l'application (mode développement)

Pour lancer le front-office en mode développement (avec rechargement à chaud) :

1.  Ouvrez un terminal (différent de celui du back-office).
2.  Naviguez vers le répertoire du front-office :
    ```bash
    cd Leoproto/frontend
    ```
3.  Lancez l'application Next.js :
    ```bash
    npm run dev
    # Ou si vous utilisez Yarn :
    # yarn dev
    ```
    L'application démarrera et sera accessible sur le port `3000`.

### URL d'accès à l'application (Front-office)

Une fois lancé, le front-office est accessible via votre navigateur à l'adresse suivante :

*   **Application Web:** `http://localhost:3000`

---

**Procédure complète pour lancer l'application :**

1.  **Lancer le Back-office :**
    *   Ouvrez un terminal.
    *   `cd Leoproto/backend`
    *   `./gradlew bootRun`
    *   Attendez que le back-office soit complètement démarré.

2.  **Lancer le Front-office :**
    *   Ouvrez un **nouveau** terminal.
    *   `npm install` (si ce n'est pas déjà fait)
    *   `npm run dev`
    *   Attendez que le front-office soit complètement démarré.

3.  **Accéder à l'application :**
    *   Ouvrez votre navigateur web et naviguez vers : `http://localhost:3000`

Vous devriez maintenant voir l'application front-office interagir avec le back-office.