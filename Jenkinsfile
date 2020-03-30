pipeline {
    agent any
        stages {
            stage('Initialize') {
                steps {
                    sh 'echo "Hello World"'
                        sh '''
                        echo "Multiline shell steps works too"
                        ls -lah
                        '''
                }
            }
            stage('Upload to AWS.') {
                withAWS(region:'us-east-2',credentials:'aws-static') {
                     def identity=awsIdentity();//Log AWS credentials
                     // Upload files from working directory 'dist' in your project workspace
                     s3Upload(bucket:"rakjenkinss3", file:'index.html');
                                                                                 
                }
            }
        }
}
