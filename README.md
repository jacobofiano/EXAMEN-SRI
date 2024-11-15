# EXAMEN-SRI
1. Explica métodos para 'abrir' unha consola/shell a un contenedor en execución.
Para poder abrir unha consola shell no contenedor debemos introducir o comando docker exec -it nome do contenedor bash
2. No contenedor anterior (en execución), qué opciones tes que ter usado ó arrincalo para poder interactuar coas súas entradas e salidas
3. Cómo sería un ficheiro docker-compose para que dous contenedores se comuniquen entre si nunha rede só deles?
 Seria o docker-comppose deste xeito:
services:
   app1:
     image: busybox
     commad: sleep 3600
     networks:
       - mi_network
   app2:
     image: busybox
     command: sleep 3600
     networks:
       - mi_network
networks:
  mi_network:
    driver: bridge
4. Qué tes que engadir ó ficheiro anterior para que un contenedor teña unha IP fixa?
Para que teña unha ip fixa debemos añadir o apartado de ports: que defina os portas a utilizar ou a ip a utilizar.
5. Qué comando de consola podo usar para sabe-las ips dos contenedores anteriores?
O comando a utilizar para saber as ip dos contenedores anteriores e ip addr show dentro dos contenedores
6. Cál é a funcionalidade do apartado "ports" en docker compose?
Serve para mapear e localizar os distintos contenedores na rede.
7. Para qué serve o rexistro CNAME? Pon un exemplo
A sua funcion e facer que un dominio sexa un alias para outro, definir un alias para o nome canonico. O CNAME e usado para asociar novos suddominios con dominios xa existentes de rexistro A. Util para suministrar nombre alternativos relacionado con diferentes servizos no mesmo equuipo.
8. Cómo podo facer para que a configuración dun contenedor DNS non se borre se creo outro contenedor?

9. Engade unha zoa tendaelectronica.int no teu docker DNS que teña:

