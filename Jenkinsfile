node {
    
     dir("D:/Development/Repos/Git/Java/Jenkins/workspace/Pipeline_Prueba/prueba"){
        //bat 'git branch rama2' 
        //bat 'git checkout rama2'
        //env.BRANCH_NAME = 'rama2'
        //bat 'git checkout master'
        //env.BRANCH_NAME = 'master'
        //bat 'git branch --show-current'
        stage 'promotion'
        def userInput = input(
        id: 'userInput', message: 'Digite la rama', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'feature']
        ])
        echo ("feature: "+userInput)
             
        if (userInput == 'master')
           {
              // bat 'git checkout release_v5.4.1_sprint1'
               
                   bat 'D:/pruebajenkins.txt'
                   bat 'MOVE D:/pruebajenkins.txt C:/Users/Johan/Desktop'
               
           }
           else {
               
               echo 'no estoy en la master'
           }   
     }      
      
}