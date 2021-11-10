pipeline { 
    agent any 
    stages { 
        stage('SCM Checkout') { 
            steps { 
                git 'https://gitlab.com/priyaank1671/devops_test' 
            }
        }
        stage('Building all 3 docker images') {
            steps { 
                script { 
                    sh 'docker build -t pb/web-server:latest -f Dockerfile-web .'
                    sh 'docker build -t pb/app-server:latest -f Dockerfile-app .'
                    sh 'docker build -t pb/sql-server:latest -f Dockerfile-sql .'
                }
            } 
        }

    }
}
