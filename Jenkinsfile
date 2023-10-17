pipeline{
    agent any
    environment{
        VERSION='1.0'
        SERVER_CREDENTIALS=credentials('test_credentials')
    }
    stages{
        stage("build"){
            steps{
                echo "Build Stage is executing"
                echo "Building version ${VERSION}"
            }
        }
        stage("Deploy"){
            steps{
                withCredentials(
                    [
                        usernamePassword(credentialsId:'test_credentials', usernameVariable:'USER', passwordVariable:'PWD')
                    ]
                ){
                    echo "some script using the ${USER} created above"
                }
                echo "server credentials are ${SERVER_CREDENTIALS}"
            }
        }
    }
}