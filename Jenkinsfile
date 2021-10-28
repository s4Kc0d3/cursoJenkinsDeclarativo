VERSION_DEL_PIPELINE="2.2"

PARAMETROS_DE_MI_PIPELINE=[
    // Aqui pongo mis parametros
    booleanParam (defaultValue: true, description: 'Descripción de mi parámetro', name: 'MI_PARAM_BOOLEAN'),
    string(defaultValue: 'valor por defecto', description: 'Descripción de mi parámetro de texto', name: 'MI_PARAM_TEXTO'),
    choice(choices: ['Valor1', 'Valor2', 'Valor3'], description: 'Descripción de mi parámetro', name: 'MI_PARAM_LISTA')


]

if (this.params.getOrDefault('VERSION_DEL_PIPELINE',"-1")!=VERSION_DEL_PIPELINE){
    stage('Configuración del JOB'){
        creoConfiguracion()
    }
    return
}

node {
    stage ("Etapa 1") {
        echo "Hago mis cosas"
    }
    stage ("Etapa 2") {
        echo "Hago más de mis cosas"
    }
}













def creoConfiguracion(){
    properties(
        [
            parameters(
                [
                    choice(name: 'VERSION_DEL_PIPELINE', description: 'Version del pipeline instalada', choices: [ VERSION_DEL_PIPELINE ])
                ] + PARAMETROS_DE_MI_PIPELINE
            )
        ]
    )
}


//dia 0 que ejecutase esto... cuanto valdria el param?
//    Nada no existe    En este escenario... quiero crear los params ? SI... y hacer algo más? NO
//Segunda ejecucion: 
//    1                  En este escenario. quiero crear parametros?  Pa' que... ya están
//Cargo una nueva version... donde hay otros parametros... o triggers, o cmabia valores por defecto de params
//    Nueva version va a ser la 2 del parametro VERSION_DEL_PIPELINE
//    La ejecuto...
//    Cuanto vale version instalada... el parametro? 1
//    Es igual que la que viene en mi script? NO... en este escenario tambien cargo y me piro
//Siguiente que ejecuto
//    Viene 2.. hago algo? las tareas.