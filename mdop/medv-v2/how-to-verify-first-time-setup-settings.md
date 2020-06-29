---
title: Cómo comprobar la configuración de instalación de primera vez
description: Cómo comprobar la configuración de instalación de primera vez
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813023"
---
# Cómo comprobar la configuración de instalación de primera vez


Mientras se ejecuta la prueba de la primera configuración o después de que finalice, puede comprobar la configuración que ha configurado en el área de trabajo de MED-V realizando las siguientes tareas.

**Nota:**  Para obtener información sobre cómo supervisar la finalización correcta de la configuración de la primera vez en su empresa después de la implementación, consulte [supervisión de implementaciones del área de trabajo de MED-V](monitoring-med-v-workspace-deployments.md).

 

**Para comprobar la configuración durante la configuración de la primera vez**

1.  Mientras se ejecuta la primera configuración, compruebe lo siguiente:

    Si especificó el modo **desatendido** , compruebe que la máquina virtual no aparece cuando se está ejecutando por primera vez la configuración.

    Si especificó el modo atendido, compruebe que aparece la máquina virtual y que se muestran todos los campos que requieren la entrada del usuario.

2.  También puede supervisar el proceso completo de primera configuración visualizando la máquina virtual cuando se está ejecutando la primera configuración. Para ello, sigue estos pasos:

    1.  Abra la consola de Windows Virtual PC.

        Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC**y, a continuación, haga clic en **Windows Virtual PC**.

    2.  Inicie MED-V si aún no se está ejecutando.

        Si aún no está presente, en un breve período de tiempo, una máquina virtual con el nombre del área de trabajo de MED-V implementada aparece en la lista de máquinas virtuales.

    3.  Haga doble clic en la máquina virtual de MED-V para abrirla.

        Puede observar la máquina virtual de MED-V cuando se está configurando y puede solucionar el problema del procedimiento de instalación mínima. Verifique la información de las distintas pantallas según vayan avanzando, como la configuración de redes, la información de unión al dominio del equipo, la configuración del agente invitado, la configuración de la configuración personal y el cierre.

    4.  La máquina virtual se cierra automáticamente cuando finaliza la configuración por primera vez.

        **Nota:**  Puede cerrar la ventana del equipo virtual en cualquier momento y la configuración de la primera vez que continúe.

         

**Para comprobar la configuración la primera vez que finaliza la configuración**

1.  Asegúrese de que la configuración de la primera vez se haya completado correctamente.

2.  Compruebe que el área de trabajo de MED-V esté configurada correctamente.

    1.  Abra la consola de Windows Virtual PC.

        Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC**y, a continuación, haga clic en **Windows Virtual PC**.

    2.  Haga doble clic en el área de trabajo de MED-V instalada.

        Si el área de trabajo de MED-V ya está ejecutando una aplicación virtual, es posible que se le pregunte si desea cerrar la aplicación antes de abrir la máquina virtual.

    3.  En el área de trabajo MED-V, haga clic con el botón secundario en **mi PC**y, a continuación, haga clic en **propiedades**.

    4.  Compruebe que el área de trabajo de MED-V se unió al dominio correcto. Si es aplicable a su organización, pruebe unirse a un dominio especificando dos dominios diferentes para comprobar que el dominio invitado es reemplazado por el dominio host.

    5.  Compruebe que el área de trabajo de MED-V se unió a la unidad organizativa del dominio que especificó.

    6.  Si especificó la máscara de nombre de equipo, compruebe que el nuevo nombre de equipo coincide con el que se especificó.

3.  Compruebe que la configuración regional que especificó es correcta.

    1.  En el área de trabajo de MED-V, haga clic en **Inicio** y, después, en **Panel de control**.

    2.  Compruebe la configuración especificada, por ejemplo, la **fecha y la hora** y la configuración **regional y de idioma**.

**Nota:**  Si encuentra algún problema al comprobar la configuración de la primera vez que se configura, consulte [operaciones de solución de problemas](operations-troubleshooting-medv2.md).

 

Después de comprobar que la configuración de la primera configuración es correcta, puede probar otras configuraciones del área de trabajo de MED-V para comprobar que funcionan como se pretende, como la publicación de aplicaciones y el redireccionamiento de direcciones URL.

Una vez que haya completado todas las pruebas de su paquete de área de trabajo de MED-V y haya comprobado que funciona como se espera, puede implementar el área de trabajo de MED-V en su empresa.

## Temas relacionados


[Cómo probar la publicación de aplicaciones](how-to-test-application-publishing.md)

[Cómo comprobar el redireccionamiento de la dirección URL](how-to-test-url-redirection.md)

[Implementación del paquete del área de trabajo de MED-V](deploying-the-med-v-workspace-package.md)

[Administrar la configuración del área de trabajo de MED-V](manage-med-v-workspace-settings.md)

 

 





