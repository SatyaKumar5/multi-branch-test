pipeline {
 
    stages {
     stage("Build"){
            steps {
                    sh """
                    echo "test"
                    cat Jenkinsfile
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
stage('Image Scan') {
            steps {
                //Put your image scanning tool 
                echo 'Image Scanning Start'
            }
            post{
                success{
                    echo "Image Scanning Successfully"
                }
                failure{
                    echo "Image Scanning Failed"
                }
            }
        }
stage("Deploy to Production"){
            when {
                branch 'master'
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
}
