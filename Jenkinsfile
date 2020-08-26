pipeline {
    agent any 
    environment {
        AWS_SECRET_KEY = credentials('aws-secret-key')
    }    
    stages {
        stage('Static Analysis') {
            steps {
                echo "Running static analysis ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo "AWS_SECRET_KEY: ${env.AWS_SECRET_KEY}"
            }
        }
        stage('Compile') {
            steps {
                echo 'Compile the source code' 
            }
        }
        stage('Security Check') {
            steps {
                echo 'Run the security check against the application' 
            }
        }
        stage('Run Unit Tests') {
            steps {
                echo 'Run unit tests from the source code' 
            }
        }
        stage('Run Integration Tests') {
            steps {
                echo 'Run only crucial integration tests from the source code' 
            }
        }
        stage('Publish Artifacts') {
            steps {
                echo 'Save the assemblies generated from the compilation' 
            }
        }
    }
}
