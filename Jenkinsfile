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
        stage('UNIT Testing'){

            steps{

                script{

                    sh 'mvn test'
                }
            }
        }
        stage('Integration Testing'){

            steps{

                script{

                    sh 'mvn verify -DskipUnitTests'
                }
            }
        }
        stage('MAVEN build'){

            steps{

                script{

                    sh 'mvn clean install'
                }
            }
        }
        stage('Static code analysis'){

            steps{

                script{

                   withSonarQubeEnv(credentialsId: 'sonar-token') {
                    sh 'mvn clean package sonar:sonar'
                    } 
                }
            }
        }
    }
}