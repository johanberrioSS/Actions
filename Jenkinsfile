node {
    
     dir("D:/Development/Repos/Git/Java/Actions"){
        
        stage 'verification'
        def userInput = input(
        id: 'userInput', message: 'Digite la rama', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'feature']
        ])
        echo ("feature: "+userInput)
             
        if (userInput == 'feature_v5.4.1')
           {
                //bat 'git checkout feature_v5.4.1'
                bat 'git branch --show-current'
                bat 'D:/Ejecutables/Model_v5/Exec/1_Restore_newdatabase.bat'
                bat 'git commit -m "prueba" D:/Development/Repos/Git/Java/Actions/johan.txt'
           }
           else {
               
               echo 'no estoy en la rama principal feature de la versión.'
           }   
     }      
      
}
