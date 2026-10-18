# CasaSalute

Desktop application written in Java with JavaFX for the Software Engineering course at the University of Verona (February 2025 exam session). It manages a local health centre: patients, doctors, nurses, bookings, visits and medical reports, with a separate view for each type of user.

I wrote all of the code. The project report was written together with two classmates.

## Repository contents

- `CasaSalute 4.zip` – the full project (Maven, Java 21, JavaFX 21)
- `Specifiche.pdf` – assignment and requirements (in Italian)
- `relazione.pdf` – project report (in Italian)

## How to run it (macOS)

You only need Java 21. JavaFX and the other libraries are downloaded automatically by Maven the first time you run the project.

### 1. Install Java 21

Check if you already have it:

```bash
java -version
```

If it doesn't say `21` (or higher), install it, for example with Homebrew:

```bash
brew install openjdk@21
```

or download the macOS installer of **Temurin 21** from [adoptium.net](https://adoptium.net/).

### 2. Get the project

```bash
git clone https://github.com/cIaudja/casasalute-javafx.git
cd casasalute-javafx
unzip "CasaSalute 4.zip"
cd "CasaSalute 4"
```

### 3. Start the app

From inside the `CasaSalute 4` folder:

```bash
chmod +x mvnw
./mvnw clean javafx:run
```

`chmod` is only needed the first time (unzipping can remove the permission to run `mvnw`). The first run takes a while because it downloads Maven and the dependencies.

**Important:** always start the app from the `CasaSalute 4` folder. The data is stored in text files under `src/main/txt/` and is read with relative paths, so starting from another folder means the app finds no data.

### Alternative: IntelliJ IDEA

1. *File → Open…* and select the `CasaSalute 4` folder (the one with `pom.xml`). IntelliJ imports it as a Maven project.
2. *File → Project Structure → Project* and set the SDK to Java 21.
3. Open the *Maven* panel on the right, then *Plugins → javafx → javafx:run* (double-click).

## Logging in

The app opens on the login screen. The sample users (doctors, nurses, patients) are stored in the text files in `src/main/txt/`; the front-desk account is defined in `LoginController.java`.
