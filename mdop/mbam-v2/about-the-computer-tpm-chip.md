---
title: Información sobre el Chip TPM del equipo
description: Información sobre el Chip TPM del equipo
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823531"
---
# Información sobre el Chip TPM del equipo


BitLocker proporciona protección adicional cuando se usa con un chip módulo de plataforma segura (TPM). El chip de TPM es un componente de hardware que los fabricantes del equipo instalan en muchos equipos nuevos. Administración y supervisión de Microsoft BitLocker (MBAM) usa BitLocker, además del chip de TPM, para proporcionar protección adicional de los datos y asegurarse de que su equipo no ha sido manipulado.

## Cómo configurar su TPM


Al iniciar el Asistente para el cifrado de unidad BitLocker en el equipo, BitLocker busca un chip de TPM si su organización ha configurado BitLocker para usar un chip de TPM. Si BitLocker encuentra un chip TPM compatible, es posible que se le pida que reinicie el equipo para habilitar el chip TPM para usarlo. Tan pronto como se haya reiniciado el equipo, siga las instrucciones para configurar el chip TPM en el BIOS (el BIOS es una capa anterior a Windows del software de su equipo).

Después de configurar BitLocker, puede obtener acceso a información adicional sobre el chip de TPM si abre la herramienta opciones de cifrado de BitLocker en el panel de control de Windows y, a continuación, selecciona **Administración de TPM**.

**Nota:**  Para tener acceso a esta herramienta, debe tener credenciales administrativas en el equipo.

 

En un error de TPM, un cambio en el BIOS o ciertas actualizaciones de Windows, BitLocker bloqueará el equipo y le será necesario que se comunique con el servicio de asistencia para desbloquearlo. Debe proporcionar el nombre del equipo, así como el dominio del equipo. El servicio de asistencia puede proporcionarle un archivo de contraseñas que puede usar para desbloquear el equipo.

## Solución de problemas de TPM


Si se produce un error de TPM, el cambio en el BIOS o ciertas actualizaciones de Windows, BitLocker bloqueará el equipo y tendrá que ponerse en contacto con el Departamento de soporte técnico para desbloquearlo. Debe proporcionar el nombre del equipo, así como el dominio del equipo. El servicio de asistencia puede proporcionarle un archivo de contraseñas que puede usar para desbloquear el equipo.

## Temas relacionados


[Ayuda a los usuarios finales para administrar BitLocker](helping-end-users-manage-bitlocker.md)

[Uso del PIN o contraseña](using-your-pin-or-password.md)

 

 





