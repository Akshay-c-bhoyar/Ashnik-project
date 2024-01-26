# Hello World Kubernetes Project

This project deploys a "Hello World" application on Kubernetes using Ansible. It includes the deployment of a Dockerized Nginx server, creation of TLS/SSL certificates, and setting up an Ingress controller for access.

## Prerequisites

- [Docker](https://www.docker.com/get-started)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Helm](https://helm.sh/docs/intro/install/)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Instructions

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Akshay-c-bhoyar/Ashnik-project.git
   cd Ashnik-project
   ```

2. **Run Ansible Playbook:**

   ```bash
   ansible-playbook -i localhost, -c local ansible/playbook.yaml
   ```

3. **Access the Application:**

   Once the deployment is complete, you can access the "Hello World" application through the configured Ingress.

   - Local Environment: [http://localhost](http://localhost)

4. **Customization:**

   - You can customize the Docker image used for the "Hello World" application by modifying the `k8s-manifests/hello-world.yaml` file. After customizing spply following commands
      -  $ kubectl apply -f hello-world.yml
      -  $kubectl get pods

   - Update the TLS/SSL certificates in the `certs` folder if needed.
      -  openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout tls.key -out tls.crt

## Notes

- The Ansible playbook automates the deployment process. Ensure that you have the necessary dependencies installed.

## License

This project is licensed under the [MIT License](LICENSE).
