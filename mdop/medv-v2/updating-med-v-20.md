---
title: Actualización de MED-V 2.0
description: Actualización de MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823731"
---
# <span data-ttu-id="f3403-103">Actualización de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="f3403-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="f3403-104">Ayude a proteger el sistema aplicando las actualizaciones de seguridad adecuadas para Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f3403-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="f3403-105">Actualización de MED-V</span><span class="sxs-lookup"><span data-stu-id="f3403-105">Updating MED-V</span></span>


<span data-ttu-id="f3403-106">Puede actualizar MED-V de forma interactiva, por el usuario final o silenciosamente usando un sistema electrónico de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="f3403-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="f3403-107">La instalación del agente de host MED-V actualiza el agente de host MED-V y, a continuación, actualiza el área de trabajo MED-V si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f3403-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="f3403-108">El agente de host MED-V y el agente invitado se mantienen sincronizados. Si las aplicaciones se ejecutan desde el área de trabajo de MED-V mientras se actualiza el agente de host MED-V, se debe reiniciar el equipo host para completar la actualización.</span><span class="sxs-lookup"><span data-stu-id="f3403-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="f3403-109">Si no se está ejecutando ninguna aplicación, MED-V se reinicia automáticamente y la actualización se completa sin reiniciar el equipo host.</span><span class="sxs-lookup"><span data-stu-id="f3403-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="f3403-110">Si está actualizando MED-V mediante un sistema de distribución de software electrónico, puede controlar el comportamiento de reinicio.</span><span class="sxs-lookup"><span data-stu-id="f3403-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="f3403-111">Para ello, suprima el reinicio si escribe **Reboot = "ReallySuppress"** en el símbolo del sistema al instalar MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="f3403-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="f3403-112">Después, configure el sistema electrónico de distribución de software para capturar el código de retorno de 3010 (que indica que es necesario reiniciar) y realizar el comportamiento de reinicio.</span><span class="sxs-lookup"><span data-stu-id="f3403-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="f3403-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3403-113">Related topics</span></span>


[<span data-ttu-id="f3403-114">Referencia técnica de MED-V</span><span class="sxs-lookup"><span data-stu-id="f3403-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





