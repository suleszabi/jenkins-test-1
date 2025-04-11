pipeline {
    
    agent any
    
    stages {
        
        stage('build') {
            steps {
                sh("ls -al")

                sh("docker run --rm --network=host -i -v $PWD:/workdir jetbrains/intellij-http-client -L VERBOSE -e dev -v api-test/test-env.json api-test/test.http")
            }
        }
        
    }
    
}
