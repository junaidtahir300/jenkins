pipeline {
    agent any
    environment{
        name = 'junaid'
    }
    parameters{
        string(name: 'email', defaultValue:'Your EMail Here Please', description: "The Correct one")
        booleanParam(name: 'gender', description: "Are you Male ?")
        choice(name: 'city',choices:['Islamabad','Rawalopindi'] ,description: "Tell your city")
    }
    stages {
        stage('Hello Run a Command') {
            environment{
                name = "tahir"
            }
            steps {
                sh '''
                echo "hello world"
                date
                pwd
                ls
                echo "name=  ${name}, email = ${email}"
                '''
            }
        }
        stage('test') {
            input {
                message "hi how are you ?"
                ok "FIne ?"
            }
            steps {
                echo "we are testing now and name = ${name}"
            }
        }
        stage('deploying') {
            steps {
                echo 'deploying on server'
            }
        }
    }
    post {
        always {
            echo "ALL DONE BROTHER"
        }
        failure{
            echo "Sorry you were not able to"
        }
        success{
            echo "Ahaaa, Good"
        }
    }
}
