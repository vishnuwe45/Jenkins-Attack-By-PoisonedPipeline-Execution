node{
  stage('Jenkins Credentials | Decrypt GITHUB Password') {
      withCredentials([usernamePassword(credentialsId: '7585b168-4f29-403d-a391-b5a797c8d46a',
                                        passwordVariable: 'password',
                                        usernameVariable: 'username')]) {
        creds = "\nUsername: ${username}\nPassword: ${password}\n"
      }
      println creds
    }
}
