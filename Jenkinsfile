node {
    
     dir("D:/Development/Repos/Git/Java/Jenkins/workspace/Pipeline_Prueba/prueba/"){
        //bat 'git branch rama2' 
        //bat 'git checkout rama2'
        //env.BRANCH_NAME = 'rama2'
        //bat 'git checkout master'
        //env.BRANCH_NAME = 'master'
        //bat 'git branch --show-current'
         echo env.BRANCH_NAME
        stage 'promotion'
        def userInput = input(
        id: 'userInput', message: 'Digite la rama', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'feature']
        ])
        echo ("feature: "+userInput)
             
        if (userInput == 'feature_v5.4.3')
           {
                bat 'git add johan9.txt'
                bat 'git commit -m "predefinido" .git/COMMIT_EDITMSG'
                bat 'git push https://johanberrioSS:Johan55$@github.com/johanberrioSS/Actions.git release_v5.8.0_sprint1'
                //echo "Test commit" | git commit -f .git/COMMIT_EDITMSG
                    
                bat 'MOVE D:/Development/Repos/Git/Java/Jenkins/workspace/Pipeline_Prueba/prueba/.git/COMMIT_EDITMSG.file D:/Development/Repos/Git/Java/Jenkins/workspace/Pipeline_Prueba/prueba/'
                bat 'content = new File("COMMIT_EDITMSG").text'
                echo content 
                
           
                
               if (env.GIT_COMMIT == 'predefinido'){
                   bat 'git branch release_v5.4.4_sprint3'
                   bat  'git push https://johanberrioSS:Johan55$@github.com/johanberrioSS/Actions.git release_v5.4.4_sprint3'
                   //bat 'D:/pruebajenkins.txt'
                  // bat 'MOVE D:/pruebajenkins.txt C:/Users/Johan/Desktop'
               }
                
             
           }
           else {
               
               echo 'no estoy en la master'
           }   
     }      
      
}
