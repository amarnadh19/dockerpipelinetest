pipeline {
    agent none
    stages {
        stage('Build') {
            input {
                message "press ok to continue"
                submitter "amar"
                parameters {
                    string(name: 'username', description: "Only lead or SME has permissions")
                }
            }
            steps {
                echo "user:$username said ok"
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'mytest' }
            }
        }
    }
}
