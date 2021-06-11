node {
  
      '


      dir("D:/Development/Repos/Git/Java/Actions"){
        
        bat '@echo off'

        bat 'set pal1-old=rojo'
        bat 'set pal1-new=negro'
        bat 'set pal2-old=casa'
        bat 'set pal2-new=departamento'
        
        bat 'set file=D:/Development/Repos/Git/Java/Actions/texto.txt'
        bat 'echo  Muestro el Archivo de texto Original'
        bat 'echo --------------------------------------'
        bat 'type texto.txt'
        bat 'echo --------------------------------------'

        bat 'for /f "tokens=*" %%a in (texto.txt) do call :wri %%a'
        bat 'type "texto.txt.bak" > "texto.txt"'
        bat 'del /f /q /a "texto.txt.bak"'

        bat 'echo.'
        bat 'echo    Muestro el Archivo ya modificado'   
        bat 'echo --------------------------------------'
        bat 'type texto.txt'
        bat 'echo --------------------------------------'
        bat 'pause'

        bat 'goto :eof'

        bat ':wri'
        bat 'set lin=%*'
        bat 'call set lin=%%lin:%pal1-old%=%pal1-new%%%'
        bat 'call set lin=%%lin:%pal2-old%=%pal2-new%%%'
        bat 'echo %lin%>>"texto.txt.bak"'
        bat 'goto :eof'
      }
    }
