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
        }    
        
        /*echo "---------------------------------------"
        echo file
        echo "---------------------------------------"

        for /f "tokens=*" %%a in (%file%) do call :wri %%a
        type "%file%.bak" > "%file%"
        del /f /q /a "%file%.bak"

        echo "."
        echo    "Muestro el Archivo ya modificado"   
        echo "--------------------------------------"
        type %file%
        echo "--------------------------------------"
        pause

        goto :eof

        :wri
        set lin=%*
        lin=%%lin:%pal1-old%=%pal1-new%%%
        echo %lin%>>"%file%.bak"
goto :eof*/
    
    bat '@echo off'
        bat 'title ler documento'

        color fc

        bat ':leer'
        bat 'set /p nombre="Escribe el nombre del documento de texto:"'
        bat 'for /f "tokens=1,2* delims=," %%i in (%nombre%.xml) do (echo %%i)'
        bat 'pause>nul'

        bat 'goto leer'
           
          
      
}
