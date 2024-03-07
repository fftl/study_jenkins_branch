pipeline {
    agent any

    stages(){
        stage('Hello') {
            steps {
                script {
                    // Docker ps 명령어 실행
                    def dockerPsOutput = sh(script: 'docker ps', returnStdout: true).trim()
                    
                    // 출력 결과를 echo로 처리
                    echo "Docker ps output: ${dockerPsOutput}"
                }
            }
        }
    }
}
