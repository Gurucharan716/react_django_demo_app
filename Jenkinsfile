pipeline {
    agent {label "dev-agent"}
    stages {
        stage("code clone") {
            steps {
                git url: "https://github.com/Gurucharan716/react_django_demo_app.git", branch: "main"
            }
        }
        stage("Build and test") {
            steps {
               sh "docker build . -t gurucharan22/react-django-app:latest"
            }
        }
        stage("Dokcer login and push image") {
            steps {
                echo "logging into docker"
                withCredentials([usernamePassword(credentialsId:"dockerHub",passwordVariable:"dockerHubPassword",usernameVariable:"dockerHubUser")]) {
                   sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPassword}"
                   sh "docker push gurucharan22/react-django-app:latest"
               }
            }
        }
         stage("Deploy") {
            steps {
               sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
