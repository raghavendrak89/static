pipeline {
    agent any
        stages {
            stage('Upload to AWS.') {
                steps {
                    sh 'uploading to S3'
                    sh '''
                        ls -lrth
                       '''
                    withAWS(region:'us-east-2',credentials:'aws-static') {
                         s3Upload(bucket:"rakjenkinss3", file:'index.html');
                    }                                                             
                }
            }
        }
}
