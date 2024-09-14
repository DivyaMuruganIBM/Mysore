pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/DivyaMuruganIBM/Mysore.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'
                sh 'echo "Your HTML project doesn\'t require any build step!"'
            }
        }
        stage('Deploy') {
            steps {
                // Replace with the appropriate deployment command for your environment
                sh 'ibmcloud login --apikey RjEjRyFVdk2JNSfR_W7Tbm4S89_p39xeQr7YLvnmvFgt'
                sh 'ibmcloud cos object-put --bucket my-html-project-mysore --key index.html --file path/to/local/index.html'
            }
        }
    }
}
