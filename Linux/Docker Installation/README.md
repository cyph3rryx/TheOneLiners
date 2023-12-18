# Docker Installation

This script automates the installation of Docker Engine on Ubuntu-based systems. Follow the steps below to ensure a smooth installation process.

## Usage

1. **Preparation**: Update package lists and install necessary dependencies.

    ```bash
    sudo apt update -y
    sudo apt install ca-certificates curl gnupg lsb-release -y
    sudo mkdir -m 0755 -p /etc/apt/keyrings
    ```

2. **Add Docker GPG Key**: Download and add the Docker GPG key to the system.

    ```bash
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
    ```

3. **Add Docker Repository**: Add the Docker repository to the list of package sources.

    ```bash
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```

4. **Install Docker Engine**: Update package lists again and install Docker Engine, Docker CLI, Containerd, Docker Buildx, and Docker Compose.

    ```bash
    sudo apt update -y
    sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
    ```

5. **Add User to Docker Group**: Add the current user to the Docker group to run Docker commands without sudo. Note that you need to log out and log back in for the group changes to take effect.

    ```bash
    sudo usermod -aG docker $USER
    echo '[!] You need to log out and log back in for the group changes to take effect.'
    ```

6. **Test Docker Installation**: Run a simple Docker container to verify the successful installation.

    ```bash
    docker run hello-world
    ```

## Notes

- This script is designed for Ubuntu-based systems.
- Ensure that you have the necessary permissions to execute the script.
- Make sure to follow the usermod instructions to apply group changes.
