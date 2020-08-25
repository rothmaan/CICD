pipline {
    agent { lable 'kubepod'}
    
    stage {
        

        stage('Checkout Source') {
            steps {
                git url:'https://github.com/rothmaan/cicd.git', branch:'master'
            }
        }
        stage('Deploy App') {
            steps { 
                script {
                    kubernetesDeploy(configs: "nginx.yaml, kubeconfigId: "myconfig")
                }
            }
        } 
     }  
}
