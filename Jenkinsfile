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
    
        
    
        dir("D:/Development/Repos/Git/Java/FocussSCM/focussSCM/src/com/focussscm/client/gwt"){
            
            bat 'set old="<set-property name="user.agent" value="safari"/>"'
            bat 'set nuevo="<!-- <set-property name="user.agent" value="safari"/> -->"'
            //bat 'file=FocussClient.gwt.xml'
            bat 'FocussClient.gwt.xml'
            /*bat '@echo off'
                bat 'title leer documento'

                bat ':leer'
                bat 'for /f "tokens=1,2* delims=," %%i in (FocussClient.gwt.xml) do (echo %%i)'
                bat 'pause>nul'*/

            
        
        echo "---------------------------------------"
        //echo file
        echo "---------------------------------------"

        bat 'for /f "tokens=*" %%a in (FocussClient.gwt.xml) do call :wri %%a'
        bat 'type "%FocussClient.gwt.xml%.bak" > "%FocussClient.gwt.xml%"'
        bat 'del /f /q /a "%FocussClient.gwt.xml%.bak"'

        echo "."
        echo    "Muestro el Archivo ya modificado"   
        echo "--------------------------------------"
        bat 'type %FocussClient.gwt.xml%'
        echo "--------------------------------------"
        pause

        bat 'goto :eof'

        bat ':wri'
        bat 'set lin=%*'
        bat 'lin=%%lin:%old%=%new%%%'
        bat 'echo %lin%>>"%FocussClient.gwt.xml%.bak"'
    
        bat 'goto :eof'
    
        }
           
          
      
}
