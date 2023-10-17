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
                        usernamePassword(credentials:'test_credentials', USER: usernameVariable, PWD: passwordVariable)
                    ]
                ){
                    echo "some script using the ${USER} and ${PWD} created above"
                }
            }
        }
    }
}