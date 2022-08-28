# containerized-nodejs-dev-environment
A template to containerize nodejs and use it as development environment in combination with Docker and WSL2.

_(Note: personally I created this template to create and develop NuxtJS applications as I'm currently learning this framework. Adaptions may be necessary for other purposes.)_

## Pre-requisites
- Docker (Desktop)
- WSL2

## Starting the container

In WSL2 you can execute `sh run-docker-compose.sh`. It'll launch a docker command and you'll enter the container in the configured working directory.

From this point on, you're good to go to start executing node related commands, e.g. `npm init nuxt-app <name>`.

## Development with Visual Studio Code

- Install the [Remote Development Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) for Visual Studio Code, to be able to develop on a Windows host machine, but use the WSL2 file system.
- In WSL2 navigate to the desired directory and enter the command `code .`. _(Alternatively you could also open Visual Studio Code by navigating to the network drive e.g. `\\wsl$\<distribution>\home\<user>`.)_

## Troubleshooting

Should Visual Studio Code give 'access denied' type errors when creating folders or files, run this command: `sudo chown -R <your_linux_distro_username> ~`

## License

See [LICENSE](/LICENSE).