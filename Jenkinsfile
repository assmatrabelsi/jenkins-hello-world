pipeline {
    agent any
    triggers {
        pollSCM('* * * * *') // Vérification chaque minute
    }
    stages {
        stage('Cloner le dépôt') {
            steps {
                git ''https://github.com/assmatrabelsi/jenkins-hello-world.git
            }
        }
        stage('Exécuter mon code  Java') {
            steps {
                script {
                    sh 'javac HelloWorld.java'
                    sh 'java HelloWorld'
                }
            }
        }
        stage('Exécuter mon code Python') {
            steps {
                script {
                    sh 'python3 hello_world.py'
                }
            }
        }
    }
}
