pipeline {
    
    agent any
    
    stages {
        
        stage('build') {
            steps {
                sh docker run --rm --network="host" -i -t -v $PWD/api-test:/workdir jetbrains/intellij-http-client -L VERBOSE -e dev -v test-env.json test.http
            }
        }
        
    }
    
}
