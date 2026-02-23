# OPERACIÓN – PROYECTO RYKUO WEB

## 1️⃣ Objetivo

Proporcionar instrucciones claras para la operación del proyecto **Rykuo Web** en producción, incluyendo:

- Monitoreo del sistema  
- Verificación de funcionamiento  
- Reinicios y actualizaciones  
- Manejo de logs  
- Procedimientos de respaldo y restauración  

Este documento permite que el sistema funcione de manera continua, segura y controlada.

---

## 2️⃣ Verificación Inicial

Después del despliegue, realizar:

1. Acceder al proyecto desde un navegador:

https://rykuo-web.vercel.app/

2. Verificar páginas principales:
- Inicio  
- Sobre Nosotros  
- Productos  
- Servicios  
- Cotización dinámica  
- Contacto
3. Probar funcionalidades dinámicas:
- Cotizador funciona correctamente  
- Formulario de contacto envía los mensajes  
- Google Analytics registra visitas  

---

## 3️⃣ Logs y Monitoreo

### 3.1 Logs de Astro / Node.js

- Si se ejecuta con **PM2**:
```bash
pm2 logs rykuo-web

Si se ejecuta con npm run dev:

npm run dev

Revisar consola para errores de ejecución

3.2 Logs de Nginx (si aplica)
sudo tail -f /var/log/nginx/access.log
sudo tail -f /var/log/nginx/error.log
3.3 Señales de alerta

Página no carga → revisar puertos, logs de Nginx o PM2

Formulario no envía → revisar API key y variables de entorno

Errores en consola → revisar dependencias o JS del frontend

4️⃣ Reinicio del Sistema
4.1 Reinicio con PM2
pm2 restart rykuo-web
4.2 Reinicio manual (servidor de desarrollo)
kill <PID_NODE>
npm run dev
4.3 Reinicio de Nginx
sudo systemctl restart nginx
5️⃣ Actualización del Proyecto

Entrar a la carpeta del proyecto:

cd /var/www/rykuo-web

Obtener cambios desde el repositorio oficial:

git fetch --all
git checkout v1.0
git pull origin main

Reinstalar dependencias si se añadieron nuevas:

npm install

Reconstruir proyecto:

npm run build

Reiniciar servidor (PM2 / Nginx):

pm2 restart rykuo-web
sudo systemctl restart nginx
6️⃣ Backups y Restauración
6.1 Respaldo del proyecto

Carpeta completa del proyecto:

tar -czvf rykuo-web-backup-$(date +%F).tar.gz /var/www/rykuo-web
6.2 Restauración desde backup
tar -xzvf rykuo-web-backup-YYYY-MM-DD.tar.gz -C /var/www/rykuo-web
cd /var/www/rykuo-web
npm install
npm run build
pm2 restart rykuo-web
6.3 Variables de entorno

Revisar .env después de restaurar, asegurando que contiene las claves correctas

7️⃣ Mantenimiento Preventivo

Revisar logs diariamente

Confirmar funcionamiento de formularios y cotizador

Verificar Google Analytics y tráfico web

Actualizar dependencias y Node.js periódicamente

Realizar backup semanal completo

8️⃣ Contactos y Soporte

Responsable técnico del proyecto: Julio Samuel Torres Garate

Email / Slack / Teléfono: julio.torres.ga@tecsup.edu.pe