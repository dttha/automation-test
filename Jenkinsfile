pipeline {
    agent any
    parameters { booleanParam(name: 'pullCode', defaultValue: false, description: 'Tích chọn để pull code mới nhất trên github') }
    
    stages {
        stage('Pullcode'){
            when {
                expression { return params.pullCode }
            }
            steps {
                git(url: "https://github.com/dttha/automation-test.git", branch: "main")
            }
        }
        stage('Build') {
            steps {
                echo "Build với parameter pullCode = ${params.pullCode}"
            }
        }
    }
}
