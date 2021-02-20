pipeline {
    agent any 

    // environment {
    //     // DOCKER_ID=credentials('DOCKER_ID')
    //     // DOCKER_PASSWORD=credentials('DOCKER_PASSWORD')
    // }

    //allow trigger from github to invoke jenkins
    triggers {
        githubPush()
    }

    stages {
        stage('Build') { 
            steps {
                // docker build -t jpk912/jenkins-test . 
                retry(3) {
                    sh '''#!/bin/bash
                    echo "Building image..."
                    
                ''' 
                }
                timeout(time: 300, unit:'SECONDS'){
                    sh 'sleep 10'
                }
            }
        }
        stage('Test') { 
            steps {
                // 
                sh '''#!/bin/bash
                    echo "no test scripts jiofjaiojf"
                ''' 
            }
        }
        stage('Deploy') { 
            steps {
                retry(3) {// echo "$DOCKER_PASSWORD" | docker login -u "$DOCKER_ID" --password-stdin
                //docker push jpk912/jenkins-test-repo
                //log in and push to docker hub
                sh '''#!/bin/bash
                    echo "deploying........"
                '''
                }
            }
        }
    }
}