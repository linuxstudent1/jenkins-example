pipeline {
    agent any

    stages {
        stage ('val') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('eric') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('yolly') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
