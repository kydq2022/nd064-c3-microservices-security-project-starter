sudo useradd  minikue
sudo passwd minikue
sudo usermod -aG docker minikue
sudo userdel -r minikue


docker run --pid=host -v /etc:/etc:ro -v /var:/var:ro -t docker.io/aquasec/kube-bench:latest --version 1.18