node {
    
     dir("D:/Development/Repos/Git/Java/FocussSCM"){
        
        stage 'verification'
        def userInput = input(
        id: 'userInput', message: 'Digite la rama', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'feature']
        ])
        echo ("feature: "+userInput)
             
        if (userInput == 'feature_v5.4.1')
           {
                bat 'git checkout feature_v5.4.1'
                bat 'git branch --show-current'
                
                bat 'CD D:/Ejecutables/Model_v5/Exec'
                bat 'MOVE D:/Ejecutables/Model_v5/Exec/1_Restore_newdatabase.bat D:/Development/Repos/Git/Java/FocussSCM'
                bat 'D:/Development/Repos/Git/Java/FocussSCM/1_Restore_newdatabase.bat'
                //bat 'content = new File("COMMIT_EDITMSG").bat'
                // echo content 
                
           
                   //bat  'git push https://johanberrioSS:Johan55$@github.com/johanberrioSS/Actions.git release_v5.4.4_sprint3'
                   bat 'D:/Development/Repos/Git/Java/FocussSCM/README_FILE.txt'
                  // bat 'MOVE D:/pruebajenkins.txt C:/Users/Johan/Desktop'
               
                
             
           }
           else {
               
               echo 'no estoy en la master'
           }   
     }      
      
}
