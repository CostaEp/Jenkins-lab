pipeline {
    agent any

    stages {
        stage('first stage') {
            steps {
                echo "hello world build id is : ${BUILD_ID}"
                script {
                    def name = "costa"
                    def age = 41
                    def greeting = "Hello , ${name}"
                    echo greeting
                }
            }
        }

        stage('second stage') {
            steps {
                sh ''' ls -la
                        mkdir -p jenkins/logs && cd jenkins/logs
                        for name in costa lev alex; do
                            echo "Hello , $name" >> jenkins/logs/logs.txt
                        done
                    '''
                script {
                    def names = ["costa", "lev", "alex"]
                    for (name in names) {
                        echo "Hello, ${name}"
                    }
                }
            }
        }
    }
}