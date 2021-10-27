pipeline {
    agent any;
    
    stages {
        stage('Etapa 1') {
            steps {
                echo 'Dentro de la Etapa 1'
            }
            post {
                echo 'Despues de la Etapa 3, si va bien'
            }
        stage('Etapa 2') {
            stages {
                stage('Etapa 2.1') {
                    step {
                        echo 'Dentro de la Etapa 2.1'
                    }
                    post {}
                }
                stage('Etapa 2.2') {
                    step {
                        echo 'Dentro de la Etapa 2.2'
                        echo 'Esta etapa gneera una explosión gigantescamente aberrante !!!! ;)'
                        sh 'exit 1'
                    }
                    post {
                        success {
                            echo "La etapa 2.2 acabó guay"
                        }
                        failure {
                            echo "La Etapa 2.2 acabó fatalmente mal"
                        }
                        always {
                            echo "La etapa acabó"
                        }
                    }
                }
            }
            steps {
                echo 'Dentro de la Etapa 2'
            }
            post {}
        }
        stage('Etapa 3') {
            steps {
                echo 'Dentro de la Etapa 3.'
            }
            
        }
    }
    post {
        always {
            echo 'Al acabar siempre'
        }
        success {
            echo 'Al acabar si todo ha ido bien'
        }
        failure {
            echo 'Al acabar si algo ha ido mal'
        }
    }
}