pipeline {

    agent any

    stages{

        stage('Git checkout'){

            script{

                git branch: 'main', url: 'https://github.com/hesblac/Demo_java_counterapp.git'
            }
        }
    }
}