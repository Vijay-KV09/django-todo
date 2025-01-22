pipeline{
    agent any


    stages{
        stage('Pulling the Github repo'){
            steps{
                git url: '',
                branch: 'main'
            }
        }
        stage('Building a Docker Imgae'){
            steps{
                echo 'Image is Building'
                sh 'docker build -t todoapp .'
            }
        }
        stage('running the container'){
            steps{
                echo 'Running the container'
                sh 'docker run -d -p 80:80 todoapp'
            }
        }
    }
}
