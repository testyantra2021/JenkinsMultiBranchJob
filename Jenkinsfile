pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    // sh 'mvn clean compile'
                    //bat 'mvn clean compile'
                    def mvnHome =  tool name: 'maven-3', type: 'maven'   
                    bat "${mvnHome}/bin/mvn clean compile"
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    // sh 'mvn test'
                    // bat 'mvn test'
                    def mvnHome =  tool name: 'maven-3', type: 'maven'   
                    bat "${mvnHome}/bin/mvn test"
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    // sh 'mvn deploy'
                    // bat 'mvn deploy'
                    def mvnHome =  tool name: 'maven-3', type: 'maven'   
                    bat "${mvnHome}/bin/mvn deploy"
                }
            }
        }
    }
}
