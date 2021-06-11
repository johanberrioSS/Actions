node {
  
      bat '@echo off'

      bat 'set pal1-old=rojo'
      bat 'set pal1-new=negro'
      bat 'set pal2-old=casa'
      bat 'set pal2-new=departamento'


      dir("D:/Development/Repos/Git/Java/Actions"){
        
        bat 'set file=D:\Development\Repos\Git\Java\Actions\texto.txt'
        bat 'echo  Muestro el Archivo de texto Original'
        bat 'echo --------------------------------------'
        bat 'type %file%'
        bat 'echo --------------------------------------'

        bat 'for /f "tokens=*" %%a in (%file%) do call :wri %%a'
        bat 'type "%file%.bak" > "%file%"'
        bat 'del /f /q /a "%file%.bak"'

        bat 'echo.'
        bat 'echo    Muestro el Archivo ya modificado'   
        bat 'echo --------------------------------------'
        bat 'type %file%'
        bat 'echo --------------------------------------'
        bat 'pause'

        bat 'goto :eof'

        bat ':wri'
        bat 'set lin=*'
        bat 'call set lin=lin:pal1-old=pal1-new'
        bat 'call set lin=lin:pal2-old=pal2-new'
        bat 'echo lin>>"%file%.bak"'
        bat 'goto :eof'
      }
    }
