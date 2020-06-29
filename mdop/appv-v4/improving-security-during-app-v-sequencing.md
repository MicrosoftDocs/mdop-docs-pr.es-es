---
title: Mejora de la seguridad durante la secuenciación de App-V
description: Mejora de la seguridad durante la secuenciación de App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816360"
---
# <span data-ttu-id="203b1-103">Mejora de la seguridad durante la secuenciación de App-V</span><span class="sxs-lookup"><span data-stu-id="203b1-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="203b1-104">Empaquetar aplicaciones para la secuencia es la mayor tarea en curso en una infraestructura de App-V.</span><span class="sxs-lookup"><span data-stu-id="203b1-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="203b1-105">Como esta tarea está en curso, debe considerar cuidadosamente la creación de directivas y procedimientos para realizar el seguimiento de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="203b1-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="203b1-106">En App-V 4.5, durante la secuenciación, puede capturar listas de control de acceso (ACL) en los activos de archivo de la aplicación virtualizada.</span><span class="sxs-lookup"><span data-stu-id="203b1-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="203b1-107">Análisis de virus en el secuenciador</span><span class="sxs-lookup"><span data-stu-id="203b1-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="203b1-108">Es recomendable instalar el software de digitalización en el equipo de secuenciación y, después, analizar el equipo en busca de virus y malware.</span><span class="sxs-lookup"><span data-stu-id="203b1-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="203b1-109">Una vez que el equipo de secuenciación se digitalice y esté libre de virus o malware, deshabilite el software de análisis, incluido todo el software de detección antivirus y de malware, en el equipo de secuenciación antes de la secuencia de cualquier aplicación.</span><span class="sxs-lookup"><span data-stu-id="203b1-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="203b1-110">Esto acelera el proceso de secuencia y evita que se detecten los componentes de software de análisis durante la secuenciación y se incluyen en el paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="203b1-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="203b1-111">Captura de ACL en archivos (NTFS)</span><span class="sxs-lookup"><span data-stu-id="203b1-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="203b1-112">El secuenciador captura los permisos NTFS (las ACL) de los archivos que se supervisan durante la fase de instalación de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="203b1-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="203b1-113">(Antes de la publicación de App-V 4.5, las ACL no se capturaban como parte del proceso de secuencia). Esta nueva característica permite que se ejecuten ciertas aplicaciones para los usuarios con un bajo nivel de permisos que normalmente requeriría privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="203b1-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="203b1-114">Esta característica también permite que el ingeniero de secuenciación Capture la configuración de seguridad identificada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="203b1-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="203b1-115">Si no se aplica la configuración recomendada por el proveedor, podría dejar la aplicación abierta para atacar o hacer un uso indebido por parte de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="203b1-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="203b1-116">Para obtener información sobre si debe implementar una aplicación con ACL abiertas, consulte el grupo de soporte técnico de aplicaciones o el proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="203b1-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="203b1-117">**Importante**  Aunque el secuenciador captura las ACL de NTFS durante la supervisión de la fase de instalación de la secuenciación, no captura las ACL para el registro.</span><span class="sxs-lookup"><span data-stu-id="203b1-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="203b1-118">Los usuarios tienen acceso total a todas las claves del registro para las aplicaciones virtuales excepto los servicios.</span><span class="sxs-lookup"><span data-stu-id="203b1-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="203b1-119">Sin embargo, si un usuario modifica el registro de una aplicación virtual, ese cambio se almacena en una ubicación específica ( `uservol_sftfs_v1.pkg` ) y no afectará a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="203b1-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="203b1-120">Durante la fase de instalación, un ingeniero de secuenciación puede modificar los permisos predeterminados de los archivos si es necesario.</span><span class="sxs-lookup"><span data-stu-id="203b1-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="203b1-121">Una vez completado el proceso de secuenciación, pero antes de guardar el paquete, el ingeniero de secuencias puede elegir exigir los descriptores de seguridad que se capturan durante la fase de instalación.</span><span class="sxs-lookup"><span data-stu-id="203b1-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="203b1-122">Es recomendable exigir el cumplimiento de los descriptores de seguridad si ninguna otra solución permite que la aplicación se ejecute correctamente una vez virtualizada.</span><span class="sxs-lookup"><span data-stu-id="203b1-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





