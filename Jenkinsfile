pipeline {
    agent {
        label 'ansible'
    }
    stages {
        stage('Install molecule') {
            steps {
                sh 'pip3 install molecule'
            }
        }
        stage('Install docker') {
            steps {
                sh 'pip3 install molecule_docker'
            }
        }
        stage('Molecule test') {
            steps {
                sh '/home/joos/.local/bin/molecule test'
            }    
        }
    }
}
