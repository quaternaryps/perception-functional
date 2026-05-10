sudo apt-get update

# Java (Temurin or OpenJDK 17+)
sudo apt-get install -y openjdk-17-jdk curl git unzip

# Clojure CLI
curl -L https://github.com/clojure/brew-install/releases/latest/download/linux-install.sh \
  -o /tmp/clojure-install.sh
chmod +x /tmp/clojure-install.sh
sudo /tmp/clojure-install.sh

# microk8s
sudo snap install microk8s --classic
sudo usermod -aG microk8s $USER
sudo chown -f -R $USER ~/.kube || true

# Enable basic microk8s addons
microk8s status --wait-ready
microk8s enable dns storage

# Docker (for building images)
sudo apt-get install -y docker.io
sudo usermod -aG docker $USER
