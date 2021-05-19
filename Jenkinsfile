node {
    
     dir("D:/Development/Repos/Git/Java/Jenkins/workspace/Pipeline_Prueba/prueba"){
        //bat 'git branch rama2' 
        bat 'git checkout rama2'
        branch = bat 'git branch --show-current'
          
        if (branch == 'rama2')
           {
               echo 'estoy en la rama' branch
           }
           else {
               //build 'Declarative pipeline'
               echo branch
           }   
     }      
      
}