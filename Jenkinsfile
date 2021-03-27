node {
    
    def app
    
    stage('Clone repository') {
        /* Clone repository to our workspace */

        checkout scm
    }
     stage('cf login') {
        /* Clone repository to our workspace */

        sh "cf login -a https://api.sys.tas490.aquaseclabs.com --skip-ssl-validation -u aquapoc -p 'Password1' -o POC -s POC-space"
    }
    
    stage('cf get env') {
        /* Clone repository to our workspace */

        sh "cf staging-environment-variable-group"
    }

    stage('cf push') {
        /* This builds the app */

        sh "cf push"
    }
    
    stage ('cf env') {
        sh "cf env test-php"
    }
}
