 stage('Deploy to Staging Environment'){
            steps{
                build job: 'Deploy-Application-Staging-Environment-pipeline'

            }
            
        }
        stage('Deploy to Production Environment'){
            steps{
                timeout(time:5, unit:'DAYS'){
                    input message:'Approve PRODUCTION Deployment?'
                }
                build job: 'Deploy-Application-Production-Environment-pipeline'
            }
        }
