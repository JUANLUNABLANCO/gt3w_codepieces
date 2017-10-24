# gt3w_codepieces
trozos de codigo



# gotth3way
para hacer pruebas con git
@url_generic: 	https://github.com/
@name 		: 	JUANLUNABLANCO/
@repository : 	gotth3way.git

@url_remote : 	[@url_generic][@name][@repository]

//crear un repositorio local
>git init
//clonar un repositorio en local desde un remoto
>git clone [@url_remote]
//muestra los remotos que tienes
>git remote -v 
//crea un nuevo repositorio
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