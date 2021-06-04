node {
    
     dir("D:/Development/Repos/Git/Java/FocussSCM"){
        
         
        stage 'verification'
        def userInput = input(
        id: 'userInput', message: 'Digite la rama', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'feature']
        ])
        echo ("feature: "+userInput)
                  
           bat 'git checkout ' + userInput
           bat 'git branch --show-current'
           bat 'cd D:/Ejecutables/Model_v5/Exec'
           bat 'D:/Ejecutables/Model_v5/Exec/1_Restore_newdatabase.bat'
           bat 'cd D:/Development/Repos/Git/Java/FocussSCM'
     }      
      
}
