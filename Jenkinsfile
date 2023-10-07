pipeline {
    agent any
    parameters {
          string(name: 'PLANET', defaultValue: 'Earth', description: 'Which planet are we on?')
          string(name: 'GREETING', defaultValue: 'Hello', description: 'How shall we greet?')
        }
        triggers {
        echo "Test"
        }
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Buid') {
            steps {
                echo 'Building'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Release') {
            steps {
                echo 'Releasing'
            }
        }
    }
}
