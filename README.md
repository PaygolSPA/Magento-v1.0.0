# PAYGOL
## _Magento_

Magento es una potente plataforma para lanzar sitios de compra y venta de productos online. Algunas de las empresas de eCommerce más grandes del mercado utilizan esta herramienta para mejorar sus sitios webs

## Requisitos
- Versión mínima Magento: 2.4.3
- Versión mínima de PHP para el plugin: 7.5

## Instalación


1. Descargar el archivo .zip del plugin.(El servidor debe contar con Magento 2.4.3 instalado).
2. Descomprimir el plugin de Paygol dentro de "path_base_magento"/app/code/ (con un cliente FTP, ej: FileZilla).
3. Desde el terminal (SSH), posicionarse en public_html (dentro del servidor)

4. Luego, ejecutar los siguientes comandos para habilitar las dependencias del módulo
- composer config repositories.paygol-core "path_base_magento"/app/code/Paygol/PaygolMagento/paygol-core
- ccomposer require kdu/paygolcore
- composer install
- composer dump-autoload
5. Por último, ejecutar los siguientes comandos para activar el módulo
- php bin/magento module:enable Paygol_PaygolMagento --clear-static-content
- php bin/magento setup:upgrade
- php bin/magento setup:di:compile (este paso puede demorar)
- php bin/magento setup:static-content:deploy -f
- php bin/magento cache:flush

6.Ya dentro de Magento, ir hacia la sección "Stores", luego entrar a "Configuration".

![paygol](http://cdn.paygol.com/images/plugins/magento/01.png)

7.En "Configuration", seleccionar "Sales" y luego "Payment Methods".
![paygol](http://cdn.paygol.com/images/plugins/magento/02.png)
![paygol](http://cdn.paygol.com/images/plugins/magento/03.png)

8.Una vez dentro, en "Merchant Country" se debe seleccionar el país de origen de tu tienda, luego en "Other Payments", se debe buscar Paygol Spa

![paygol](http://cdn.paygol.com/images/plugins/magento/04.png)

9.Cambiar el "Environment" a "Production" configurar el módulo con el “Token Service/Service ID” y “Token Secret/Secret Key” entregados por Paygol

![paygol](http://cdn.paygol.com/images/plugins/magento/05.png)
![paygol](http://cdn.paygol.com/images/plugins/magento/06.png)
10.Tu e-commerce está listo para aceptar pagos a través de Paygol. Si tienes algún problema o duda con la instalación del plugin, puedes contactarnos al correo soporte@paygol.com
![paygol](http://cdn.paygol.com/images/plugins/magento/07.png)

