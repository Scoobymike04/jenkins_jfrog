pipeline{
    agent any
    tools {
        jfrog 'Jfrog_cli'
    }
    stages {
        stage ('Testing') {
            steps {
                jf '-v' 
                jf 'c show'
                jf 'rt ping'
                sh 'touch test-file'
                jf 'rt u test-file Jfrog_cli/'
                jf 'rt bp'
                jf 'rt dl Jfrog_cli/test-file'
            }
        } 
    }
}