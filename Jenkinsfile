node {
     //se crea una variable que llevara la versión actual que se va a desplegar    
        stage 'version'
        def version = input(
        id: 'version', message: 'Versión a desplegar', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'feature', description: 'Environment', name: 'version']
        ])
     //se crea una variable que llevará el sprint actual  
        stage 'ciclo'
        def ciclo = input(
        id: 'version', message: 'Ciclo de la versión', parameters: [
        [$class: 'TextParameterDefinition', defaultValue: 'sprint1', description: 'Environment', name: 'ciclo']
        ])
    
   // se cambia al directorio del repositorio
   dir("D:/Development/Repos/Git/Java/FocussSCM"){
          
           //se cambia a la rama de la versión a desplegar
           bat 'git checkout ' + version
           //se muestra la rama actual
           bat 'git branch --show-current'
     
      //se cambia al directorio donde se encuentre el bat de restauración y actualización de la newdatabase
      dir("D:/Development/Repos/Git/Batch/CheckUpdateScript"){
           //se restaura y actualiza la newdatabase 
          // bat '0_Check_Update_Script.bat'
           
       } 
    
      //se cambia al directorio donde se encuentra el bat que modifica el archivo FocussClient.gwt.xml
      dir("D:/Simple Solutions S.A.S/Developers - General/Archivos de Despliegue"){
         
           //bat 'Change_Focuss_GWT_File.bat'
           //bat 'localpropertiesChange.bat'
      } 
        
      //se cambia al directorio desde donde se ejecuta la meta mvn_focussscm_deployScript_install
      dir("D:/Development/Repos/Git/Java/FocussSCM/focussSCMDataBaseScripts"){
        
        bat 'mvn -Dmaven.test.skip=true clean install'
        bat 'START D:/Development/Repos/Maven/com/focussscm/dbversion.update/0.0.1'
        }    
        
      //se cambia al directorio desde donde se ejecuta la meta mvn_focussscm_redeploy
      dir("D:/Development/Repos/Git/Java/FocussSCM/focussSCMParent"){
           
           //bat 'mvn -P dbupdate -D db.user=sa -D db.password=123 -Dmaven.test.skip=true clean install gwt:clean gwt:compile install package cargo:redeploy'
        bat 'START "" "D:/Simple Solutions S.A.S/Servidores - FocussWizard/Installers/FocussSCM/v5.5.0/installers"'
      } 
           
           //se realiza el commit al repositorio del archivo de creación de la versión. 
           //bat 'git commit -m "creation File" "D:/Development/Repos/Git/Java/FocussSCM/focussSCMDataBaseScripts/resources/CurrentVersionScripts/+'Create_SCM_'+'version'+'.sql'
           //bat 'git push https://johanberrioSS:contraseña@github.com/johanberrioSS/Actions.git feature'+version
           
           //se crea la rama de liberación de ciclo
           //bat 'git branch release_' + version +'_'+ ciclo
           //bat 'git push https://johanberrioSS:contraseña@github.com/johanberrioSS/Actions.git release_'+version+'_'+ciclo
              
   }
}
