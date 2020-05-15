# Rebasing entre branches remotos
## Ejercicios

## Trabajar sobre las carpetas de clonado local (Ver LocalRemotes)

## 1. Partir de una rama master sin divergencias
* Partir de un HEAD remoto y crear nuevas ramas en cada cliente:
~~~
# en cada cliente:
git checkout master
git pull
git checkout -b branchClient1
~~~

## 2. Efectuar modificaciones en un nuevo archivo, pero en el mismo en cada cliente
* En client-1/my-files crear un archivo testRebase.txt
* Escribir en el mismo una línea "cliente 1" y dos saltos de línea
* commitear y pushear branchClient1
* En client-2/my-files repetir en el mismo archivo pero con salto, "cliente 2", salto
* En client-3/my-files lo mismo pero con salto, "cliente-3", salto

## 3. Mergear el primer branch pusheado en server
* Tomar el primer branch (recordar que no hay divergencia ya que no hay nuevos commits en master):
~~~
# Fast-forward merge:
git merge branchClient1
~~~

## 4. Resolver la primer divergencia
* En client-2 actualizar la base de branchClient2
~~~
git checkout master
git pull
git checkout branchClient2
git rebase master
# Si se presentan conflictos resolverlos
git push origin branchClient2 --force-with-lease
~~~

## 5. Mergear el segundo branch en server
* Como se actualizó la base y se resolvieron conflictos en el cliente también será Fast-forward:
~~~
git merge branchClient2
~~~

## 7. Crear un nuevo commit en client-3
* Agregar una nueva línea de texto en testRebase.txt
* confirmar y subir a server

## 8. Actualizar base en client-3
* Recordar que ahora hay dos commits de divergencia en master y dos commits de divergencia en client-3 y puede ser necesario resolver conflictos en estos dos últimos

## 9. Mergear el tercer branch en server.

## 10. Eliminar branches de feature remotos y locales en cada cliente.
