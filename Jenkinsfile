pipeline{
    agent {
  label 'ansible'
    }
    stages {
        stage('Clear_Start') {
            steps {
                deleteDir()
            }
        }
        stage('Git') {
            steps {
                git branch: 'main', url: 'https://github.com/vladislav-arzybov/vector-role.git'
            }
        }
                stage('Test') {
            steps {
                sh 'molecule test'
            }
        }
                stage('Clear_Final') {
            steps {
                deleteDir()
            }
        }
    }
}
