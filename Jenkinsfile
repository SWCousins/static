pipeline {
    agent any
    stages {
        stage('Upload to AWS'){
            steps {
                withAWS(region:'us-east-2',credentials:'Jenkins') {
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-bucket-1133')
            }
        }
    }
}
}