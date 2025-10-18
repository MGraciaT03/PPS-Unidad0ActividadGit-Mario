# Mario Gracia Torres Actividad 0: Sistemas de control de versiones
===============


## 1 Creación de Proyecto y repositorio

Utilizamos los comandos mkdir para crear la carpeta y entrar en ella con cd

```
mkdir PPS-Unidad0ActividadGit-$Mario
cd PPS-Unidad0ActividadGit-$Mario
```
<img width="auto" height="120" alt="mkdir" src="https://github.com/user-attachments/assets/66422174-6953-4fce-8098-c12930a66b17" />

Entramos a Github con nuestra cuenta y creamos un nuevo repositorio publico. Lo llamamos PPS-Unidad0ActividadGit-$Mario

<img width="auto" height="600" alt="repositorio" src="https://github.com/user-attachments/assets/b2e90c71-675e-46f5-9f27-bcf85dee131d" />
<img width="auto" height="500" alt="imagen" src="https://github.com/user-attachments/assets/8e35b18b-6115-46b9-8239-4efb1f17f8a1" />

para clonarlo o subirlo a Debian, copiamos el codigo ssh y lo pegamos en la maquina virtual donde queremos crear el repositorio

<img width="631" height="auto" alt="githubssh" src="https://github.com/user-attachments/assets/2a8c401c-2662-40d5-a6af-7b5d1deb8b2c" />

<img width="auto" height="272" alt="creandorepositorio" src="https://github.com/user-attachments/assets/0085828a-11bd-4cc2-89c3-a605b0482e70" />

## 2 Estructurando el proyecto

Vamos a empezar a crear la estructura de nuestro proyecto

Creamos la carpeta de calculator y varios ficheros como  ```__init__.py``` ```gui.py```  ```mkdocs.yml``` ```requiriments.txt```

dejando una estructura asi:
1. La estructura del proyecto debe de ser la siguiente:

PPS-Unidad0ActividadGit-Mario/   
├── calculator/   
│   ├── __init__.py   
│   └── gui.py   
├── docs/   
│   └── index.md   
├── mkdocs.yml   
├── requirements.txt   


<img width="317" height="auto" alt="calculator" src="https://github.com/user-attachments/assets/5e88d63d-3e43-4e0e-a7f7-002699e1ba38" />

Comprobamos el estado con git status y vemos la organizacion del directorio
```
git status
```
<img width="373" height="auto" alt="status1" src="https://github.com/user-attachments/assets/d9e4ecdc-43d3-46f1-a331-94561457508e" />

```
git status
```

<img width="465" height="563" alt="tree" src="https://github.com/user-attachments/assets/e9afe8b3-bd0c-4463-886f-68b4f38ed302" />

Modificamos los ficheros  ```__init__.py``` ```gui.py```  ```mkdocs.yml``` ```index.md``` ```requiriments.txt```

Hacemos los cambios al repositorio subiendo un commit

<img width="auto" height="247" alt="ficheros" src="https://github.com/user-attachments/assets/886f23bc-0ed2-4ab4-a10c-26dd91d7da0e" />


<img width="auto" height="303" alt="repositorio" src="https://github.com/user-attachments/assets/b2f6ae8f-16db-4dc7-9590-c0518bc3679d" />


## 3 Ignorando archivos del repositorio

1. Creamos la ucarpeta con nombre `Excluded`

2. creamos un archivo con nombre excluido.txt 

<img width="auto" height="267" alt="imagen" src="https://github.com/user-attachments/assets/b1880e37-916b-49cc-a336-bcf3ba090397" />

3. Crea un archivo con nombre .gitignore 

4. Indicamos en el .gitignore que los archivos con extensión **.txt** y el directorio `Excluded`

5. Hacemos los cambios al repositorio

<img width="auto" height="497" alt="imagen" src="https://github.com/user-attachments/assets/d29b9790-8632-4f6e-a018-710cf23811b2" />


## 4Levantar un pequeño Servidor Web con PHP

<img width="auto" height="2o2" alt="imagen" src="https://github.com/user-attachments/assets/ef65222d-055e-45c8-afba-91c5bd9535e3" />

hacemos los cambios al fichero ```index.html```

<img width="auto" height="512" alt="imagen" src="https://github.com/user-attachments/assets/a4dd23a9-e416-4151-97bd-6158f8eb3def" />

Refrescamos los cambios con git status 

<img width="auto" height="100" alt="imagen" src="https://github.com/user-attachments/assets/1d8ab040-0dfc-4fb9-8dee-f6e23a5f6b68" />

usamos gitt diff para modificar el fichero index.html para que cambie el texto mostrado y ver que ha cambiado el mensaje en la web

<img width="auto" height="500" alt="imagen" src="https://github.com/user-attachments/assets/2c9ce33d-58b3-456b-9e59-a11834ddb0f1" />

Usamos restore para restaurar el mensaje original de la web 

<img width="auto" height="163" alt="imagen" src="https://github.com/user-attachments/assets/bf960aed-726f-4c8f-bea2-a5aa12fd972e" />

Finalmente hacemos los cambios y los subimos

## 5 Git log

1. Para mostrar los logs generales
```bash 
git log
```
<img width="auto" height="300" alt="imagen" src="https://github.com/user-attachments/assets/52d54c99-bd7b-4aa2-af80-5b6b521f8743" />

1. Para mostrar los logs de los últimos 3 commits y los logs utilizando el modificador ``--pretty`

```bash 
git log -3
git log --pretty=oneline
```
<img width="auto" height="311" alt="imagen" src="https://github.com/user-attachments/assets/9f807dcd-4041-4469-8c21-bf1749362c7a" />


1. Para mostrar los logs de los últimos 2 commits donde se vean las diferencias de cada una de las entradas y los logs de las modificaciones realizadas en el último día.
```bash 
git log -p -2
git log --since=1.day
```

<img width="auto" height="353" alt="imagen" src="https://github.com/user-attachments/assets/92cb22e8-6120-4fd8-8b04-7ce31127a706" />


## 6 Ramas

1. Listamos las ramas existentes.
```bash 
git branch --list
```
<img width="452" height="auto" alt="imagen" src="https://github.com/user-attachments/assets/dcd27ddd-8b7a-47ee-9fd9-0f9f15aea64b" />


1. Elimina el archivo index.html.save y creamos una rama dev a la rama actual

```bash
git rm index.html.save
git commit -am "eliminando index.html.save"
git push origin main
git chekout -b dev
```
<img width="425" height="auto" alt="imagen" src="https://github.com/user-attachments/assets/3be3c58a-6c91-40bb-9d93-d9ad9e7b50a5" />


1. Subimos los cambios al respositorio remoto a la rama `dev`  

```bash 
git push origin dev
```
En este caso, vemos las ramas `main` y `dev` son diferentes.

<img width="510" height="auto" alt="imagen" src="https://github.com/user-attachments/assets/0ae23a34-5a0d-489e-a8a3-bc16b4839abd" />






