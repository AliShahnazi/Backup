---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}


# Ampliación de la capacidad de la caja fuerte
{: #expandcapacity}

Los usuarios actuales de {{site.data.keyword.BluSoftlayer_full}} pueden ampliar el tamaño de su caja fuerte hasta un máximo de 4000 GB. No es necesario que creen un duplicado ni que migren los datos manualmente a un volumen más grande. El proceso de aumento del límite no causa ninguna parada ni falta de acceso.

## Solicitud de un aumento

1. Inicie la sesión en la [consola de {{site.data.keyword.cloud_notm}}](https://{DomainName}/){:new_window} y pulse el icono de **Menú** de la parte superior izquierda. Seleccione **Infraestructura clásica**.<br/>
   También puede iniciar la sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){:new_window}.
2. Pulse **Almacenamiento** > **Copia de seguridad** para visualizar los servidores con servicio de copia de seguridad.
3. Seleccione la caja fuerte que desea ampliar.
4. Pulse **Acciones** y seleccione **Modificar {{site.data.keyword.backup_notm}}**.
5. En la pantalla siguiente, seleccione el nuevo tamaño y pulse **Actualizar**.

## Facturación

Los datos de facturación del volumen se actualizan automáticamente para añadir al ciclo de facturación actual la diferencia prorrateada del nuevo precio. Luego se factura el nuevo importe completo durante el siguiente ciclo de facturación.

Se puede utilizar el mismo proceso para reducir el tamaño de {{site.data.keyword.backup_notm}}.
{:tip}
