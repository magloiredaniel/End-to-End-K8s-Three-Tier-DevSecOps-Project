# Déploiement d'applications Web à trois tiers sur AWS EKS à l'aide d'AWS EKS, ArgoCD, Prometheus, Grafana et Jenkins

## Présentation du projet:

Bienvenue dans le guide du projet DevSecOps Kubernetes de bout en bout ! Dans ce projet complet, nous passerons en revue le processus de mise en place d'une architecture robuste à trois niveaux sur AWS en utilisant Kubernetes, les meilleures pratiques DevOps et des mesures de sécurité. Ce projet vise à fournir une expérience pratique dans le déploiement, la sécurisation et la surveillance d'un environnement d'application évolutif.

![Three-Tier Banner](assets/Three-Tier.gif)

Bienvenue dans le projet de déploiement d'applications Web à trois niveaux ! 🚀

Ce référentiel héberge l'implémentation d'une application Web à trois niveaux utilisant ReactJS, NodeJS et MongoDB, déployée sur AWS EKS. Le projet couvre un large éventail d'outils et de pratiques pour une configuration DevOps robuste et évolutive.

## Table of Contents
- [Déploiement d'applications Web à trois tiers sur AWS EKS à l'aide d'AWS EKS, ArgoCD, Prometheus, Grafana et Jenkins](#déploiement-dapplications-web-à-trois-tiers-sur-aws-eks-à-laide-daws-eks-argocd-prometheus-grafana-et-jenkins)
  - [Présentation du projet:](#présentation-du-projet)
  - [Table of Contents](#table-of-contents)
  - [Application Code](#application-code)
  - [Jenkins Pipeline Code](#jenkins-pipeline-code)
  - [Jenkins Server Terraform](#jenkins-server-terraform)
  - [Fichiers manifestes Kubernetes](#fichiers-manifestes-kubernetes)
  - [Détails du projet](#détails-du-projet)
  - [Getting Started (Commencer)](#getting-started-commencer)
  - [📌 Aperçu du projet:](#-aperçu-du-projet)
  - [📌 Conditions préalables:](#-conditions-préalables)
  - [📘 Étape 1 : Nous devons créer un utilisateur IAM et générer la clé d'accès AWS](#-étape-1--nous-devons-créer-un-utilisateur-iam-et-générer-la-clé-daccès-aws)
  - [Contribuant](#contribuant)
  - [License](#license)

## Application Code
Le dossier `Application-Code` contient le code source de l'application Web à trois tiers. Plongez dans ce répertoire pour explorer les implémentations frontend et backend.

## Jenkins Pipeline Code
Dans le dossier `Jenkins-Pipeline-Code`, vous trouverez les scripts de pipeline Jenkins. Ces scripts automatisent le processus CI/CD, garantissant une intégration et un déploiement fluides de votre application.

## Jenkins Server Terraform
Explorer le dossier `Jenkins-Server-TF` pour trouver des scripts Terraform permettant de configurer le serveur Jenkins sur AWS. Ces scripts simplifient le processus de provisionnement de l'infrastructure.

## Fichiers manifestes Kubernetes
Le dossier `Kubernetes-Manifests-Files` contient les manifestes Kubernetes pour le déploiement de votre application sur AWS EKS. Comprenez et personnalisez ces fichiers en fonction des besoins de votre projet.

## Détails du projet
🛠️ **Outils explorés:**
- Terraform et AWS CLI pour l'infrastructure AWS
- Jenkins, Sonarqube, Terraform, Kubectl et plus pour la configuration CI/CD
- Helm, Prometheus et Grafana pour la surveillance (Monitoring)
- ArgoCD pour les pratiques GitOps

🚢 **Aperçu de haut niveau:**
- Configuration des utilisateurs IAM et magie Terraform sur AWS
- Déploiement Jenkins avec intégration AWS
- Création de cluster EKS et configuration de l'équilibreur de charge
- Référentiels ECR privés pour une gestion sécurisée des images
- Graphiques Helm pour une configuration de surveillance efficace
- GitOps avec ArgoCD - la cerise sur le gâteau !

📈 **Le parcours a tout couvert, de la configuration des outils au déploiement d'une application à trois tiers, en passant par la garantie de la persistance des données et la mise en œuvre de pipelines CI/CD.**

## Getting Started (Commencer)
Pour démarrer ce projet, reportez-vous à notre [GUIDE COMPLET](https://amanpathakdevops.medium.com/advanced-end-to-end-devsecops-kubernetes-three-tier-project-using-aws-eks-argocd-prometheus-fbbfdb956d1a) qui vous guide à travers la configuration des utilisateurs IAM, le provisionnement de l'infrastructure, la configuration du pipeline CI/CD, la création de cluster EKS, et bien plus encore.

## 📌 Aperçu du projet:

Dans ce projet, nous couvrirons les aspects clés suivants :

1. **Configuration de l'utilisateur IAM**: créez un utilisateur IAM sur AWS avec les autorisations nécessaires pour faciliter les activités de déploiement et de gestion.
2. **Infrastructure as Code (IaC)**: utilisez Terraform et AWS CLI pour configurer le serveur Jenkins (instance EC2) sur AWS.
3. **Configuration du serveur Jenkins**: installez et configurez les outils essentiels sur le serveur Jenkins, notamment **Jenkins** lui-même, **Docker**, **Sonarqube**, **Terraform**, **Kubectl**, **AWS CLI** et **Trivy**.
4. **Déploiement du cluster EKS**: utilisez les commandes **eksctl** pour créer un **cluster Amazon EKS**, un **service Kubernetes** géré sur AWS.
5. **Configuration de l'équilibreur de charge (Load Balancer)**: configurez AWS Application Load Balancer (ALB) pour le cluster EKS.
6. **Référentiels Amazon ECR** : créez des référentiels privés pour les images Docker frontend et backend sur **Amazon Elastic Container Registry (ECR)**.
7. **Installation d'ArgoCD**: installez et configurez **ArgoCD** pour la **livraison continue** et **GitOps**.
8. **Intégration Sonarqube**: intégrez Sonarqube pour l'analyse de la qualité du code dans le **pipeline DevSecOps**.
9. **Pipelines Jenkins**: créez des pipelines Jenkins pour déployer du code backend et frontend sur le **cluster EKS**.
10. **Configuration de la surveillance (Monitoring Setup)** : implémentez la surveillance (Monitoring) du cluster EKS à l'aide de **Helm**, **Prometheus** et **Grafana**.
11. **Déploiement de l'application ArgoCD** : utilisez ArgoCD pour déployer l'application à trois tiers, y compris les **composants de base de données**, **backend**, **frontend** et les **Ingress Components**.
12. **Configuration DNS** : configurez les paramètres DNS pour rendre l'application accessible via des sous-domaines personnalisés.
13. **Persistance des données (Data Persistence)**: implémentez des volumes persistants et des revendications de volumes persistants pour les pods de base de données afin de garantir la persistance des données.
14. **Conclusion et Monitoring** : concluez le projet en résumant les principales réalisations et en surveillant les performances du cluster EKS à l'aide de Grafana.

## 📌 Conditions préalables:

Avant de démarrer le projet, assurez-vous d'avoir les prérequis suivants :

* Un compte AWS avec les autorisations nécessaires pour créer des ressources.
* Terraform et AWS CLI installés sur votre machine locale.
* Familiarité de base avec **les principes Kubernetes, Docker, Jenkins et DevOps**.

## 📘 Étape 1 : Nous devons créer un utilisateur IAM et générer la clé d'accès AWS




https://blog.stackademic.com/advanced-end-to-end-devsecops-kubernetes-three-tier-project-using-aws-eks-argocd-prometheus-fbbfdb956d1a


## Contribuant
Nous apprécions les contributions ! Si vous avez des idées d'améliorations ou si vous rencontrez des problèmes, veuillez ouvrir une pull request ou signaler un problème.

## License
This project is licensed under the [MIT License](LICENSE).

Happy Coding! 🚀
