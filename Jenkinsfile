pipeline {
    agent {
        node {
            label 'ansible_docker'
        }
    }

    stages {
        stage('Prepare') {
            steps {
                //git branch: 'main', credentialsId: '268920f0-532b-4a18-8607-0eab59638598', url: 'https://github.com/VitalyMozhaev/mnt-homeworks-ansible-1'
                git 'https://github.com/VitalyMozhaev/mnt-homeworks-ansible-1'
            }
        }
        stage('Check') {
            steps {
                sh 'ansible --version'
            }
        }
        stage('Playbook') {
            steps {
                sh 'ansible-playbook site.yml -i inventory/test.yml'
            }
        }
    }
}
