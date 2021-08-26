pipeline {
     agent any
    stages {
     stage("Build"){
            steps {
                    sh """
                    echo "test test test tsdt"
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

stage("Deploy to Production"){
            when {
                branch 'main'
            }
            steps { 
                echo "master branch cicd"
 
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
