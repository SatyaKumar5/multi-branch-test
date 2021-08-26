pipeline {
     agent any
    stages {
     stage("Build"){
            steps {
                    sh """
                    echo "test test test tsdt test test"
                    """
                }

            post{
                success{
                    echo "Build and Push Successfully"
                }
                failure{
                    echo "Build and Push Failed"
                }
            }
        }

stage("Deploy to preprod"){
            when {
                expression { BRANCH_NAME ==~ /release\-[0-9]+\.[0-9]+/ } 
            }
            steps { 
                echo "release branch cicd"
 
             }
            post{
                success{
                    echo "Successfully deployed to Production"
                }
                failure{
                    echo "Failed deploying to Production"
                }
            }
        }
stage("Deploy to Staging"){
            when {
                branch 'develop'
            }
            steps {
                echo "develop branch cicd"
             }
            post{
                success{
                    echo "Successfully deployed to Staging"
                }
                failure{
                    echo "Failed deploying to Staging"
                }
            }
        }

    }
}
