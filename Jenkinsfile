pipeline {
        agent any
            stages {
                stage('Upload to AWS') {
                    steps{
                        withAWS(region:'us-east-2',credentials:'aws-static') {
                            sh label: '', script: 'ls'
                            s3Upload(bucket:"rakjenkinss3", workingDir:'Dist', file:'index.html');
                                                                                        
                        }
                    }
                        
                }
                 
            }
}

