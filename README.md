[![Mod Loader](https://img.shields.io/badge/Mod%20Loader-Quilt-magenta?style=for-the-badge "Quilt")](https://quiltmc.org/en/)
# Create: Astral - SMP edit

Personal edit of the Create: Astral modpack for an SMP

Suggestions and Bugs should go in [Issues](https://github.com/Aproxia-dev/Create-Astral-SMP-edit/issues), be as detailed as possible so things can be easy to add or fix!

Does not include mods, or most configs.
Just pack specific stuff which is used when compiling the pack.

## Contributing

This repository uses [packwiz](https://github.com/packwiz/packwiz), which allows a lightweight repository such as this to be built into a full modpack by downloading mods from modrinth or curse.

These instructions will be a simplified version from the [packwiz installer tutorial](https://packwiz.infra.link/tutorials/installing/packwiz-installer/), so if you run into any issues you should look there.
First, clone this repository to wherever you want and use your code editor of choice.

To start, make sure you have [Prism Launcher](https://prismlauncher.org/), or a similar launcher.

Create an instance in the launcher with just the minecraft version (1.18.2), and quilt version (0.18.10). Increase memory allocation if you want to (you probably do)

Download the packwiz installer jar from [packwiz-installer-bootstrap](https://github.com/packwiz/packwiz-installer-bootstrap/releases), and put it into the `/minecraft/` folder in the instance. If it isnt there already, you can just create a folder with that name.

Go to Edit Instance -> Settings -> Custom commands, then check the Custom Commands box and paste the following command into the pre-launch command field:

```shell
"$INST_JAVA" -jar packwiz-installer-bootstrap.jar http://localhost:8080/pack.toml
```

![image](https://user-images.githubusercontent.com/55003876/228606395-9cbdf5ac-c095-4f71-a639-3765dc906ad5.png)

Now that all of that is ready, navigate to the repository in your terminal, and run `packwiz serve`

This will host a copy of pack.toml that is updated every time it is queried, meaning that every time you start the minecraft instance, it will be able to get the most updated version of all your changes, and update the instance to match, meaning that all you need to do to reload all of your changes is to restart your minecraft instance.

If you want, you could also write a batch script that runs the jar file in a similar way to how it is run at the startup of the instance, that you could run to reload the modpack without restarting the game.

## Files you may want to edit

```md
📦
┣ 📂config //Various configs for all sorts of mods
┃ ┣ 📂ftbquests //Configs for quests
┣ 📂kubejs
┃ ┣ 📂assets
┃ ┃ ┣ 📂\* mods // Renaming items for mods
┃ ┃ ┣ 📂createastral
┃ ┃ ┃ ┗ 📂textures // Textures for custom blocks
┃ ┣ 📂client_scripts // Scripts that load for the client
┃ ┣ 📂server_scripts // All recipe changes
┃ ┣ 📂startup_scripts // Things that run on startup
┣ 📂mods // Mods
┣ 📂resourcepacks // Textures, includes some mods
┗ 📜README.md // This file! Feel free to contribute
and fix any erorrs that you see.
