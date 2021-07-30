node {
    
     dir("D:/Development/Repos/Git/Java/Actions"){
        
         
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
           //bat 'localpropertiesChange.bat'
      } 
    
      dir("D:/Development/Repos/Git/Java/FocussSCM/focussSCMDataBaseScripts"){
        
        bat 'mvn clean install'
        bat 'START D:/Development/Repos/Maven/com/focussscm/dbversion.update/0.0.1'
        }    
    
      dir("D:/Development/Repos/Git/Java/FocussSCM/focussSCMParent"){

           //bat 'mvn -P dbupdate -D db.user=sa -D db.password=123 clean install gwt:clean gwt:compile install package cargo:redeploy'
           //bat 'START D:/Simple Solutions S.A.S/Servidores - FocussWizard/Installers/FocussSCM/v5.5.0'
      } 
    
           /*bat 'git commit -m "creation File" "D:/Development/Repos/Git/Java/FocussSCM/focussSCMDataBaseScripts/resources/CurrentVersionScripts/Create_SCM_v5.5.0.sql'
           bat 'git push https://johanberrioSS:contraseña@github.com/johanberrioSS/Actions.git feature '+ userInput*/
           stage 'verification'
            def userInputdos = input(
            id: 'userInputdos', message: 'Digite la rama', parameters: [
            [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'feature']
            ])
    
    dir("D:/Development/Repos/Git/Java/Actions"){
           bat 'git branch release_' + userInputdos + '_sprint1'
           bat 'git push https://johanberrioSS:555777999@github.com/johanberrioSS/Actions.git release_'+userInputdos +'_sprint1'
    }        
   
}
