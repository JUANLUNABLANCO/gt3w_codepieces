# gt3w_codepieces
trozos de codigo



# gotth3way
para hacer pruebas con git
@url_generic: 	https://github.com/
@name 		: 	JUANLUNABLANCO/
@repository : 	gotth3way.git

@url_remote : 	[@url_generic][@name][@repository]      //https://github.com/JUANLUNABLANCO/git_test.git

//Pasos para dar para usasr correctamente git
 Download and install Git                                                       //instalar segun plataforma
  git config --global user.name "Your Name"                                     //configurar tu nombre
  git config --global user.email "youremail@gmail.com"                          //configurar el correo
  Add your public key ?                                                         //añadir la publickey ??


Next steps:

  mkdir <name_dir>                                                              //crear directorio
  cd <name_dir>                                                                 //cambiarse a ese directorio
  git init                                                                      //crear un repositorio local en este directorio
  touch README.md                                                               //crear archivo
  git add README.md                                                             //añadir al HEAD un commit
  git commit -m 'first commit'                                                  //hacer un commit
  git remote add origin git@github.com:<your_name>/<repository_name>.git        //crear el repositorio en remoto
  git push origin master                                                        //subir al remoto(origin) rama master(principal)

//mostrar la configuracion de git
>git config --list

//crear un repositorio local
>git init
//clonar un repositorio en local desde un remoto
>git clone [@url_remote]
//muestra los remotos que tienes
>git remote -v 
//crea un nuevo repositorio en tu ordenador 
>git remote add [@name][@url_remote]
//ver el estado del repositorio local
>git status
//pasar los cambios  hechos al index
>git add .
//pasar esos cambios al origin
>git commit -m "mensaje descriptivo" 
//subir cambios locales al repositorio remoto
>git push origin master
//si no te deja porque haya habido cambios previos, por otros usuarios, debes bajarte los cambios del remoto 
//a tu local
>git pull [@url_remote]
//borrar un repositorio en local
>erase .git
>sudo rm -R .git

//crear una rama nueva
>git branch nombre_rama
//activar una rama para trabajar
>git checkout nombre_rama
//tras realizar cambios en archivos quieres subir esos cambios haciendo un commit
>git add .
>git commit -a -m "cambios en nueva rama"
//subir esos cambios al remoto
>git push origin nombre_rama
//subir los cambios de la nueva rama a master
>git checkout master
>git merge nueva_rama
//tras fucionar ambas ramas en master la nueva_rama puede que quieras borrarla
>git branch -d nueva_rama


//en ocasiones tenemos este error
C:\Users\Usuario\Documents\_GitHub>git push origin master
Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

//La solucion puede venir por hacer porimero un 
>git pull https://github.com/JUANLUNABLANCO/git_test.git

//si esto no funciona, podemos editar .got/config y poner en la linea

[remote "origin"]

url = git@github.com/yourGithubUserName/yourRepo.git
//por esta otra
url = ssh://git@github.com/yourGithubUserName/yourRepo.git

fetch = +refs/heads/*:refs/remotes/origin/*

//posteriormente en vez de hacer 
>git push origin master
//haz esto otro
>git push https://github.com/JUANLUNABLANCO/git_test.git
//te preguntará username and password, en el caso que no lo acepte
//vuelve a hacer un git pull
