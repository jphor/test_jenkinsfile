pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('SCM') {
            steps {
               git branch: 'gh-pages', url: 'https://github.com/jphor/patchwork.git'
            }
        }
        stage('Check') {
            steps {
               echo "Check repo"
               sh '''
               echo "checking repo"
               ls -ltr
               '''
            }
        }
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing delivery stuff.."
                sleep 10
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
