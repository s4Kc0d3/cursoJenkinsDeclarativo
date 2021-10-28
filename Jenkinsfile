VERSION_DEL_PIPELINE = "2"

if (this.params.getOrDefault('VERSION_DEL_PIPELINE',"-1") != VERSION_DEL_PIPELINE) {
    creoConfiguracion()
    return 
}

node {
    stage("Etapa 1") {
        echo "Hago mis cosas"
    }
    stage("Etapa 2") {
        echo "Hago más de mis cosas"
    }
}


def creoConfiguracion() {
    properties(
        [
            parameters(
                [
                    choice(name: 'VERSION_DEL_PIPELINE', descripcion: 'Version del pipeline instalada', choices: [VERSION_DEL_PIPELINE]),
                    choice(name: 'OPCIONES', descripcion: 'Elija entorno', choices: ['desarrollo','produccion'])
                    // Aqui pongo el resto de params que necesite mi pipeline 
                ]    
            )
        ]
    )
}
