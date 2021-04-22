pipeline {
    agent {
      node {
        label 'workstation'
      }
    }

    environment { 
        URL = "test.femilab.com"
    }

    stages {
        stage('Stage1') {
            environment { 
                URL = "stage.femilab.com"
            }

            steps {
                sh 'Hello world!, check out URL = ${URL} ' 
            }
        }

        stage('Stage2') {
            steps {
                sh 'Lets move on, check out URL = ${URL}' 
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}