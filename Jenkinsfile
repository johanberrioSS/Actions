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
            
            /*set old="<set-property name="user.agent" value="safari"/>"
            set nuevo="<!-- <set-property name="user.agent" value="safari"/> -->"*/
            file="D:/Development/Repos/Git/Java/FocussSCM/focussSCM/src/com/focussscm/client/gwt/FocussClient.gwt.xml"
            bat 'FocussClient.gwt.xml'
            /*bat '@echo off'
                bat 'title leer documento'

                bat ':leer'
                bat 'for /f "tokens=1,2* delims=," %%i in (FocussClient.gwt.xml) do (echo %%i)'
                bat 'pause>nul'*/

        }    
        
        echo "---------------------------------------"
        echo file
        echo "---------------------------------------"

        bat 'for /f "tokens=*" %%a in (%file%) do call :wri %%a'
        bat 'type "%file%.bak" > "%file%"'
        bat 'del /f /q /a "%file%.bak"'

        echo "."
        echo    "Muestro el Archivo ya modificado"   
        echo "--------------------------------------"
        bat 'type %file%'
        echo "--------------------------------------"
        pause

        goto :eof

        bat ':wri'
        bat 'set lin=%*'
        bat 'lin=%%lin:%pal1-old%=%pal1-new%%%'
        bat 'echo %lin%>>"%file%.bak"'
goto :eof
    
    
           
          
      
}
