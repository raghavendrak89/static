pipeline {
    agent any
        stages {
            stage('S3upload') {
                steps {
                    withAWS(region:'us-east-2', credentials:'aws-static') {
                        s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'rakjenkinss3')
                                      
                    }
                        
                }
                    
            }

        }

}

