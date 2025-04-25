Explicacion del proceso de despliegue.

1. Descargar los archivos entregados en el caso de estudio

2. Probe de manera local el codigo siguiendo el paso a paso del repositorio https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab

3. Luego de probar el codigo de manera local subi estos archivos a mi repositorio en GitHub mediante Git.

4. Ingrese a Vercel y luego de iniciar sesion Importe directamente el proyecto desde mi GitHub, verificando que todo estuviera bien.

5. Luego de validar que efectivamente el despliegue se habia dado de manera correcta ingrese a https://securityheaders.com/ para evaluar el nivel de seguridad dandome cuenta que este tenia una calificacion de "D" es decir una baja.

6. Problemas Detectados
   
        Content-Security-Policy ausente
        Vulnerable a ataques de XSS y carga de contenido malicioso.
        
        X-Frame-Options ausente
        Riesgo de clickjacking (otro sitio podría embeber el tuyo en un <iframe>).
        
        X-Content-Type-Options ausente
        Navegador podría "adivinar" el tipo de contenido e interpretar scripts como ejecutables.
        
        Referrer-Policy ausente
        Se enviaban datos del Referer a sitios externos sin control.
        
        Permissions-Policy ausente
        El navegador no tenía restricciones para acceder a APIs como cámara, micrófono, etc.
7. Implementación de Medidas de Seguridad:

    Se creó un archivo llamado vercel.json en la raíz del proyecto.
  
    En este archivo se definieron las cabeceras de seguridad recomendadas por securityheaders.com.

8. Subi este archivo a el repositorio de GitHub y espere que los cambios se aplicaran para recargar la pagina de Vercel y que se aplicaran los cambios de manera correcta.

9. Me dirigi nuevamente a el enlace de la aplicacion recargando la pagina para verificar que todo funcionara.

10. Volvi a utilizar https://securityheaders.com/ para verificar la mejora mostrandome la mejora de la calificación general pasando de una "D" a una "A".

URL de la aplicacion despleagda: https://pokemon-def.vercel.app/
    
    




   
  
        

  
