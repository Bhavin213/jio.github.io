# Day 7 Answers: Understanding Package Manager and Systemctl

## Tasks

1. **Install Docker and Jenkins:**
   - Install Docker and Jenkins on your system from your terminal using package managers.

   **Answer**
     - Installing Docker
       - Update the package list and install required packages:
         ```bash
            sudo apt update
            sudo apt install apt-transport-https ca-certificates curl software-properties-common 
       - Add Docker’s official GPG key:
         ```bash
            curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -          
       - Add the Docker APT repository:
         ```bash
            sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
       - Update the package list again:
         ```bash
            sudo apt update
       - Install Docker:
         ```bash
            sudo apt install docker-ce
       - Check Docker installation:
         ```bash
            sudo systemctl status docker

     - Installing Jenkins
       - Add the Jenkins repository key to the system:
         ```bash
            curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
       - Add the Jenkins repository:
         ```bash
            sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
       - Update the package list:
         ```bash
            sudo apt update
       - Install Jenkins:
         ```bash
            sudo apt install jenkins
       - Start Jenkins:
         ```bash
            sudo systemctl start jenkins
       - Note:
         - First, check whether JAVA is installed or not.
           ```bash
              java -version
         - If you have not installed
           ```bash
              sudo apt install default-jre

   ![image](https://github.com/Bhavin213/90DaysOfDevOps/blob/master/2024/day06/image/task1.png)

2. **Write a Blog or Article:**
   - Write a small blog or article on how to install these tools using package managers on Ubuntu and CentOS.

   **Answer**
   1. Introduction:
      - Briefly introduce Docker and Jenkins.
      - Mention the operating systems (Ubuntu and CentOS) covered.
   2. Installing Docker on Ubuntu:
      - List the steps as detailed above.
   3. Installing Docker on CentOS:
      - Provide similar steps adjusted for CentOS.
   4. Installing Jenkins on Ubuntu:
      - List the steps as detailed above.
   5. Installing Jenkins on CentOS:
      - Provide similar steps adjusted for CentOS.

### Systemctl and Systemd

Systemctl is used to examine and control the state of the “systemd” system and service manager. Systemd is a system and service manager for Unix-like operating systems (most distributions, but not all).

## Tasks

1. **Check Docker Service Status:**
   - Check the status of the Docker service on your system (ensure you have completed the installation tasks above).

   **Answer**
   ![image](https://github.com/Bhavin213/90DaysOfDevOps/blob/master/2024/day06/image/task1.png)

2. **Manage Jenkins Service:**
   - Stop the Jenkins service and post before and after screenshots.

   **Answer**
   ![image](https://github.com/Bhavin213/90DaysOfDevOps/blob/master/2024/day06/image/task1.png)

3. **Read About Systemctl vs. Service:**
   - Read about the differences between the `systemctl` and `service` commands.
   - Example: `systemctl status docker` vs. `service docker status`.

   For reference, read [this article](https://www.howtogeek.com/devops/how-to-check-if-the-docker-daemon-or-a-container-is-running/#:~:text=Checking%20With%20Systemctl&text=Check%20what%27s%20displayed%20under%20%E2%80%9CActive,running%20sudo%20systemctl%20start%20docker%20).

### Additional Tasks

4. **Automate Service Management:**
   - Write a script to automate the starting and stopping of Docker and Jenkins services.

   **Answer**
   ![image](https://github.com/Bhavin213/90DaysOfDevOps/blob/master/2024/day06/image/task1.png)

5. **Enable and Disable Services:**
   - Use systemctl to enable Docker to start on boot and disable Jenkins from starting on boot.

   **Answer**
   ![image](https://github.com/Bhavin213/90DaysOfDevOps/blob/master/2024/day06/image/task1.png)

6. **Analyze Logs:**
   - Use journalctl to analyze the logs of the Docker and Jenkins services. Post your findings.

   **Answer**
   ![image](https://github.com/Bhavin213/90DaysOfDevOps/blob/master/2024/day06/image/task1.png)
