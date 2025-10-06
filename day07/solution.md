# Day 7 Answers: Understanding Package Manager and Systemctl

## Tasks

1. **Install Docker and Jenkins:**
   - Install Docker and Jenkins on your system from your terminal using package managers.

   **Answer**
     - **First-Installing Docker**
       - Set up the repository:
         ```bash
            sudo dnf -y install dnf-plugins-core
            sudo dnf-3 config-manager --add-repo https://download.docker.com/linux/fedora/docker-ce.repo
       - Install the Docker packages:
         ```bash
            sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin          
       - Start Docker Engine.
         ```bash
            sudo systemctl enable --now docker
       - Verify that the installation is successful by running the hello-world image:
         ```bash
            sudo docker run hello-world
       - Check Docker installation:
         ```bash
            sudo systemctl status docker

     - **Installing Jenkins**

       - Add the Jenkins repository:
         ```bash
            sudo wget -O /etc/yum.repos.d/jenkins.repo \ https://pkg.jenkins.io/redhat-stable/jenkins.repo
            sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
            sudo dnf upgrade
       - Add required dependencies for the jenkins package
         ```bash
            sudo dnf install fontconfig java-21-openjdk
       - Install Jenkins:
         ```bash
            sudo dnf install jenkins
            sudo systemctl daemon-reload
       - Start Jenkins:
         ```bash
            sudo systemctl enable jenkins
            sudo systemctl start jenkins
         
       - You can check the status of the Jenkins service using the command
         ```bash
            sudo systemctl status jenkins
            

   Output (Docker)
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/docker-version.png)

   Output (Jenkins)
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/jenkins-version.png)

 
### Systemctl and Systemd

Systemctl is used to examine and control the state of the “systemd” system and service manager. Systemd is a system and service manager for Unix-like operating systems (most distributions, but not all).

## Tasks

1. **Check Docker Service Status:**
   - Check the status of the Docker service on your system (ensure you have completed the installation tasks above).

   **Answer**
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/status-docker.png)

2. **Manage Jenkins Service:**
   - Stop the Jenkins service and post before and after screenshots.

   **Answer**
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/start-status-jenkins.png)
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/stop-status-jenkins.png)

4. **Read About Systemctl vs. Service:**
   - Read about the differences between the `systemctl` and `service` commands.
   - Example: `systemctl status docker` vs. `service docker status`.

   **Answer**
    - Understanding the `systemctl` and `service` Commands
      - Both `systemctl` and `service` commands are used to manage system services in Linux, but they differ in terms of usage, functionality, and the system architectures they support.
      - **`systemctl` Command**
        - `systemctl` is a command used to introspect and control the state of the `systemd` system and service manager. It is more modern and is used in systems that use `systemd` as their init system, which is common in many contemporary Linux distributions.
        - Examples:
          - Check the status of the Docker service:
            ```bash
               sudo systemctl status docker    
          - Start the Jenkins service:
            ```bash
               sudo systemctl start jenkins 
          - Stop the Docker service:
            ```bash
               sudo systemctl stop docker
          - Enable the Jenkins service to start at boot:
            ```bash
               sudo systemctl enable jenkins
             
      - **`service` Command**
        - 'service' is a command that works with the older 'init' systems (like SysVinit). It provides a way to start, stop, and check the status of services. While it is still available on systems using 'systemd' for backward compatibility, its usage is generally discouraged in favor of 'systemctl'.
        - Examples:
          - Check the status of the Docker service:
            ```bash
               sudo service docker status    
          - Start the Jenkins service:
            ```bash
               sudo service jenkins start
          - Stop the Docker service:
            ```bash
               sudo service docker stop

      - **Key Differences**
        - 1 System Architecture:
          - `systemctl` works with `systemd`.
          - `service` works with SysVinit and is compatible with `systemd` for backward compatibility.    
        - 2 Functionality:
          - `systemctl` offers more functionality and control over services, including management of the service's state (start, stop, restart, reload), enabling/disabling services at boot, and querying detailed service status.
          - `service` provides basic functionality for managing services, such as starting, stopping, and checking the status of services.
        - 3 Syntax and Usage:
          - `systemctl` uses a more unified syntax for managing services.
          - `service` has a simpler and more traditional syntax.

### Additional Tasks

4. **Automate Service Management:**
   - Write a script to automate the starting and stopping of Docker and Jenkins services.

   **Answer**
   ![image]()

5. **Enable and Disable Services:**
   - Use systemctl to enable Docker to start on boot and disable Jenkins from starting on boot.

   **Answer**
    - Enable Docker to start on boot:
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/onboot-docker.png)

    - Disable Jenkins from starting on boot:
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/onboot-jenkins.png)

6. **Analyze Logs:**
   - Use journalctl to analyze the logs of the Docker and Jenkins services. Post your findings.

   **Answer**
    - Docker Logs:
   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/docker-log.png)

    - Jenkins Logs:

   ![image](https://github.com/Vaidik-Gampawar/90DaysOfDevOps/blob/main/day07/image/jenkins-log.png)








