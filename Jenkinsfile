pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the application code from your GitHub repository using the main branch
                git branch: 'main', url: 'https://github.com/MarzouguiAhmed9/ciccdproject.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Change to the directory where the Dockerfile is located

                        sh 'docker build -t marzouguiAhmed9/cicd2:latest .'

                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {



                    sh 'docker run -d --name my-html-app222 -p 8099:80 marzouguiAhmed9/cicd2:latest'
                }
            }
        }
    }


}
