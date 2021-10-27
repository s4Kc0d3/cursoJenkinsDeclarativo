node {
    try {
        stage('Etapa 0'){
        echo 'Dentro de la Etapa 0'
        }
        stage('Etapa 1'){
            try {
                echo 'Dentro de la Etapa 1'
                if (this.params.CODIGO_SALIDA != '0') {
                   sh 'exit 1' 
                }
            }catch (exc) {
                // Este seria el caso failure del Declarativo
                echo 'Esto solo se va a ejecutar si se ha producido un error'
                echo 'Despues de la Etapa 1, si va bien'
            }finally {
                echo 'Esto se ejecutara si hay error o no'
            }
            echo 'Luego vendrian más tareas después'
              
        }
    }catch {
        echo "Se ejecuta si algun sitio de la etapa 1 ha habido un error"
    }finally {
        echo "Esto se ejecutara independientemente si ha ido bien la Etapa 1"
    }
    stage('Etapa 2'){
        echo 'Estoy en la Etapa 2'
    }
}