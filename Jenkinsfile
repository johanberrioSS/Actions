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
     } 
    
     dir("D:/Ejecutables/Model_v5/Exec"){
         
           bat '1_Restore_newdatabase.bat'
           
      } 
      dir("D:/Ejecutables"){
         
           bat 'Change_Focuss_GWT_File.bat'
           
      } 
    
        
    
    
           
          
      
}
