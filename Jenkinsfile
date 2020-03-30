pipeline {
    agent any
        stages {
            stage('Upload to AWS.') {
                steps {
                    sh 'uploading to S3'
                    withAWS(region:'us-east-2',credentials:'aws-static') {
                         def identity=awsIdentity();//Log AWS credentials
                         // Upload files from working directory 'dist' in your project workspace
                         s3Upload(bucket:"rakjenkinss3", file:'index.html');
                    }                                                             
                }
            }
        }
}
