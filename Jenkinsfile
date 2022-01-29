pipeline {
    agent any
   
    stages{
        stage("build"){
            steps{
                
                sh 'echo "Hello, World!"'
                
            }
        }
        stage("buildMore"){
            steps{
                 sh '''
                    echo "multi line text"
                    ls -lah
                    '''
            }
        }
        stage("Deploy"){
            steps{
                timeout(time:1 ,unit:'MINUTES'){
                    sh '/Users/i079243/learn/shell/hello.sh 5'
                }
                timeout(time:1 ,unit:'MINUTES'){
                    sh '/Users/i079243/learn/shell/hello.sh 32'
                }
            }
        }
    }
}
