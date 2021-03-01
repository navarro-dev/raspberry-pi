## Installing the Docker Engine on Raspbian

 1. Make sure you update, upgrade Raspbian and reboot the Pi
    ```
    sudo apt-get update && sudo apt-get upgrade
    sudo reboot now
    ```
 2. Download the convenience script and run script to install the Docker Engine
    ```
    curl -fsSL https://get.docker.com -o get-docker.sh
    ```
    ```
    sudo sh get-docker.sh
    ```
    Check installation by checking Docker version
    ```
    sudo docker --version
    ```
 3. Add non-root to Docker group, **sudo** will not be required every user runs a Docker command
    If planning to use the **pi** user, simply run
    ```
    sudo usermod -aG docker $USER
    ```

## Installing the Docker Compose on Raspbian via Python Package Installer

 1. Install dependencies
    ```
    sudo apt-get install -y libffi-dev libssl-dev
    ```
    ```
    sudo apt-get install -y python3 python3-pip
    ```
 2. Install Docker Compose
    ```
    sudo pip3 install docker-compose
    ```
    Check installation by checking Docker Compose version
    ```
    docker-compose --version
    ```
