pipeline {

    agent any

    stages{

        stage('Git checkout'){

            steps{

                script{

                    git branch: 'main', url: 'https://github.com/hesblac/Demo_java_counterapp.git'
                }

            }
        }
    }
}