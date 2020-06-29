---
title: MED-V 1.0 SP1 y notas de la versión de SP2
description: MED-V 1.0 SP1 y notas de la versión de SP2
author: dansimp
ms.assetid: 0fde8732-8ad2-483c-b094-7996ed9f2766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e90b85068faa277cd03e31963c4cad5b5a37f7a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826600"
---
# <span data-ttu-id="19015-103">MED-V 1.0 SP1 y notas de la versión de SP2</span><span class="sxs-lookup"><span data-stu-id="19015-103">MED-V 1.0 SP1 and SP2 Release Notes</span></span>


<span data-ttu-id="19015-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="19015-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="19015-105">**Nota:**  Lea estas notas de la versión minuciosamente antes de instalar la plataforma de virtualización de escritorio de Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="19015-105">**Note** Read these Release Notes thoroughly before you install the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="19015-106">Estas notas de la versión contienen información que debe tener para instalar correctamente la plataforma MED-V.</span><span class="sxs-lookup"><span data-stu-id="19015-106">These Release Notes contain information that you must have to successfully install the MED-V platform.</span></span> <span data-ttu-id="19015-107">Este documento contiene información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="19015-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="19015-108">Si hay una discrepancia entre estas notas de la versión y otra documentación de la plataforma MED-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="19015-108">If there is a discrepancy between these Release Notes and other MED-V platform documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="19015-109">Estas notas de la versión reemplazan al contenido incluido en este producto.</span><span class="sxs-lookup"><span data-stu-id="19015-109">These Release Notes supersede the content included with this product.</span></span>

 

## <span data-ttu-id="19015-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="19015-110">About the Product Documentation</span></span>


<span data-ttu-id="19015-111">Encontrará documentación completa de la plataforma de virtualización de escritorio de Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="19015-111">Comprehensive documentation for Microsoft Enterprise Desktop Virtualization (MED-V) platform is available.</span></span> <span data-ttu-id="19015-112">Consulte la guía de planeación, implementación y operaciones de virtualización de escritorio de Microsoft Enterprise.</span><span class="sxs-lookup"><span data-stu-id="19015-112">Refer to the Microsoft Enterprise Desktop Virtualization Planning, Deployment, and Operations Guide.</span></span>

## <span data-ttu-id="19015-113">Protegerse contra virus y vulnerabilidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="19015-113">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="19015-114">Para ayudarle a protegerse contra virus y vulnerabilidades de seguridad, debe instalar las últimas actualizaciones de seguridad disponibles para el nuevo software que está instalando.</span><span class="sxs-lookup"><span data-stu-id="19015-114">To help protect against security vulnerabilities and viruses, you should install the latest available security updates for any new software that you are installing.</span></span> <span data-ttu-id="19015-115">Para obtener más información, consulte el sitio web de seguridad de Microsoft en <https://go.microsoft.com/fwlink/?LinkId=3482> .</span><span class="sxs-lookup"><span data-stu-id="19015-115">For more information, see the Microsoft Security website at <https://go.microsoft.com/fwlink/?LinkId=3482>.</span></span>

## <a href="" id="what-s-new-in-med-v-1-0-sp2"></a><span data-ttu-id="19015-116">Novedades de MED-V 1,0 SP2</span><span class="sxs-lookup"><span data-stu-id="19015-116">What’s New in MED-V 1.0 SP2</span></span>


<span data-ttu-id="19015-117">MED-V 1.0 SP2 incluye las siguientes actualizaciones para las características y funcionalidades de MED-V 1.0 SP1:</span><span class="sxs-lookup"><span data-stu-id="19015-117">MED-V1.0SP2 includes the following updates to the MED-V1.0SP1 features and functionality:</span></span>

-   <span data-ttu-id="19015-118">Compatibilidad con MED-V en una estación de trabajo en chino tradicional o en chino simplificado.</span><span class="sxs-lookup"><span data-stu-id="19015-118">Support for running MED-V on a Chinese traditional or Chinese simplified workstation.</span></span>

-   <span data-ttu-id="19015-119">Compatibilidad con el cliente de MED-V 1.0 SP2 para ejecutarse en Windows 7 SP1.</span><span class="sxs-lookup"><span data-stu-id="19015-119">Support for the MED-V1.0SP2 client to run on Windows 7 SP1.</span></span>

-   <span data-ttu-id="19015-120">Se ha mejorado el rendimiento de las aplicaciones que se ejecutan en el área de trabajo de MED-V cuando los marcos de MED-V en las aplicaciones publicadas están activados.</span><span class="sxs-lookup"><span data-stu-id="19015-120">Improved performance for the applications that are running in the MED-V workspace when MED-V frames around the published applications are turned-on.</span></span> <span data-ttu-id="19015-121">Anteriormente, en algunas instancias, los marcos de MED-V tenían que desactivarse para que las aplicaciones se ejecutaran correctamente.</span><span class="sxs-lookup"><span data-stu-id="19015-121">Previously, under some instances the MED-V frames had to be turned-off for the applications to run correctly.</span></span>

## <span data-ttu-id="19015-122">Problemas conocidos con MED-V 1.0 SP1 y MED-V 1,0 SP2</span><span class="sxs-lookup"><span data-stu-id="19015-122">Known Issues with MED-V1.0 SP1 and MED-V 1.0 SP2</span></span>


<span data-ttu-id="19015-123">Esta sección proporciona la información más actualizada sobre problemas con la plataforma de virtualización de escritorio de Microsoft Enterprise (MED-V) 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="19015-123">This section provides the most up-to-date information about issues with the Microsoft Enterprise Desktop Virtualization (MED-V)1.0 SP1 platform.</span></span> <span data-ttu-id="19015-124">Estos problemas no aparecen en la documentación del producto y, en algunos casos, pueden contradicción de la documentación del producto existente.</span><span class="sxs-lookup"><span data-stu-id="19015-124">These issues do not appear in the product documentation and in some cases may contradict existing product documentation.</span></span> <span data-ttu-id="19015-125">Siempre que sea posible, estos problemas se tratan en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="19015-125">Whenever possible, these issues are addressed in later releases.</span></span>

### <span data-ttu-id="19015-126">MED-V no proporciona compatibilidad con la experiencia de usuario avanzada de Windows7</span><span class="sxs-lookup"><span data-stu-id="19015-126">MED-V does not provide Windows7 advanced user experience support</span></span>

<span data-ttu-id="19015-127">MED-V 1.0 SP1 no proporciona compatibilidad con la experiencia de usuario avanzada de Windows7, como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="19015-127">MED-V1.0 SP1 does not provide Windows7 advanced user experience support, such as the following:</span></span>

<span data-ttu-id="19015-128">El acoplamiento de las ventanas a la parte superior, izquierda o derecha no se aplica a las ventanas de la aplicación publicadas.</span><span class="sxs-lookup"><span data-stu-id="19015-128">Docking windows to the top, left, or right is not applied to published application windows.</span></span>

<span data-ttu-id="19015-129">La vista previa de la barra de tareas de Windows7 no muestra el contenido de la aplicación publicada.</span><span class="sxs-lookup"><span data-stu-id="19015-129">The Windows7 taskbar preview does not display the published application content.</span></span>

## <span data-ttu-id="19015-130">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="19015-130">Release Notes Copyright Information</span></span>


<span data-ttu-id="19015-131">La información de este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, está sujeta a cambios sin previo aviso y se proporciona con fines informativos únicamente.</span><span class="sxs-lookup"><span data-stu-id="19015-131">Information in this document, including URL and other Internet website references, is subject to change without notice, and is provided for informational purposes only.</span></span> <span data-ttu-id="19015-132">El usuario asume todo riesgo de uso o resultados del uso de este documento, y Microsoft Corporation no otorga garantías expresas ni implícitas.</span><span class="sxs-lookup"><span data-stu-id="19015-132">The entire risk of the use or results of the use of this document remains with the user, and Microsoft Corporation makes no warranties, either express or implied.</span></span> <span data-ttu-id="19015-133">Las compañías, las organizaciones, los productos, las personas y los acontecimientos de ejemplo aquí descritos son ficticios.</span><span class="sxs-lookup"><span data-stu-id="19015-133">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="19015-134">No se pretende indicar ni debe deducirse ninguna asociación con empresas, organizaciones, productos, personas o eventos reales.</span><span class="sxs-lookup"><span data-stu-id="19015-134">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span> <span data-ttu-id="19015-135">El cumplimiento de todas las leyes de propiedad intelectual vigentes es responsabilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="19015-135">Complying with all applicable copyright laws is the responsibility of the user.</span></span> <span data-ttu-id="19015-136">Sin limitación de los derechos de propiedad intelectual, ninguna parte de este documento puede ser reproducida, almacenada o introducida en un sistema de recuperación, o transmitida de ninguna forma ni por ningún medio (electrónico, mecánico, Fotocopiado, grabación o de cualquier otro modo), ni con ningún propósito, sin la autorización expresa y por escrito de Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="19015-136">Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.</span></span>

<span data-ttu-id="19015-137">Microsoft puede tener patentes, solicitudes de patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual sobre los contenidos de este documento.</span><span class="sxs-lookup"><span data-stu-id="19015-137">Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document.</span></span> <span data-ttu-id="19015-138">A excepción de lo estipulado expresamente en un contrato de licencia por escrito de Microsoft, el suministro de este documento no le otorga ninguna licencia para estas patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual.</span><span class="sxs-lookup"><span data-stu-id="19015-138">Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.</span></span>



<span data-ttu-id="19015-139">Microsoft, Microsoft Enterprise Desktop Virtualization, MS-DOS, Windows, WindowsServer, Windows Vista, Active Directory y ActiveSync son marcas comerciales registradas o marcas comerciales de MicrosoftCorporation en los Estados Unidos y/o en otros países.</span><span class="sxs-lookup"><span data-stu-id="19015-139">Microsoft, Microsoft Enterprise Desktop Virtualization, MS-DOS, Windows, WindowsServer, Windows Vista, Active Directory, and ActiveSync are either registered trademarks or trademarks of MicrosoftCorporation in the U.S.A. and/or other countries.</span></span>

<span data-ttu-id="19015-140">Los nombres de las compañías y productos reales mencionados en el presente pueden ser marcas comerciales de sus respectivos propietarios.</span><span class="sxs-lookup"><span data-stu-id="19015-140">The names of actual companies and products mentioned herein may be the trademarks of their respective owners.</span></span>

 

 





