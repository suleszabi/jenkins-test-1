pipeline {
    
    agent any
    
    stages {
        
        stage('build') {
            steps {
                sh("curl -f -L -o ijhttp.zip https://jb.gg/ijhttp/latest")

                sh("unzip ijhttp.zip")

                sh("ijhttp/ijhttp api-test/test.http --env-file api-test/test-env.json --env dev")
            }
        }
        
    }
    
}
