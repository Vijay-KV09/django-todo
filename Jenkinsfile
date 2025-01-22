pipeline{
    agent any


    stages{
        stage('Pulling the Github repo'){
            steps{
                git url: 'https://github.com/Vijay-KV09/django-todo/',
                branch: 'main'
            }
        }
        stage('Building a Docker Image'){
            steps{
                echo 'Image is Building'
                bat 'docker build -t todoapp .'
            }
        }
        stage('Running the Container'){
            steps{
                echo 'Running the container'
                bat 'docker run -d -p 8000:8000 todoapp'
            }
        }
    }
}
