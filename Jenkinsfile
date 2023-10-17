pipeline{
    agent any
    environment{
        VERSION='1.0'
        //SERVER_CREDENTIALS=credentials('jenkinsuser')
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
                        usernamePassword(credentials:'jenkins_user', usenameVariable:USER, passwordVariable:PWD)
                    ]
                ){
                    sh "some script using the ${USER} and ${PWD} created above"
                }
            }
        }
        post{
            always{
                // delete ghost/orphan files
            }
            success{

            }
            failure{

            }
        }
    }
}