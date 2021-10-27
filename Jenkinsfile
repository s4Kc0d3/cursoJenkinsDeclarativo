node {
    stage('Etapa 0'){
        echo 'Dentro de la Etapa 0'
    }
    stage('Etapa 1'){
        try {
            echo 'Dentro de la Etapa 1'
            sh 'exit 1'
        }catch (exc) {
            // Este seria el caso failure del Declarativo
            echo 'Esto solo se va a ejecutar si se ha producido un error'
            echo 'Despues de la Etapa 1, si va bien'
        }finally {
            echo 'Esto se ejecutara si hay error o no'
        }
        echo 'Luego vendrian más tareas después'
          
    }
}