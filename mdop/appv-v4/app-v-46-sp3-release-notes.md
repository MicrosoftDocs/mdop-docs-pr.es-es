---
title: Notas de la versión de App-V4.6SP3
description: Notas de la versión de App-V4.6SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819791"
---
# <span data-ttu-id="bc525-103">Notas de la versión de App-V4.6SP3</span><span class="sxs-lookup"><span data-stu-id="bc525-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="bc525-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="bc525-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="bc525-105">Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="bc525-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="bc525-106">Estas notas de la versión contienen información que le ayudará a instalar correctamente Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc525-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="bc525-107">Este documento contiene información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="bc525-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="bc525-108">Si hay una diferencia entre estas notas de la versión y otra documentación de App-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="bc525-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="bc525-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="bc525-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="bc525-110">Protegerse contra virus y vulnerabilidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="bc525-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="bc525-111">Para ayudar a protegerse contra virus y vulnerabilidades de seguridad, es importante instalar las últimas actualizaciones de seguridad disponibles para cualquier nuevo software que se instale.</span><span class="sxs-lookup"><span data-stu-id="bc525-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="bc525-112">Para obtener más información, consulte el [sitio web de seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="bc525-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="bc525-113">Problemas conocidos con Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="bc525-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="bc525-114">Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc525-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="bc525-115">Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente.</span><span class="sxs-lookup"><span data-stu-id="bc525-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="bc525-116">Cuando sea posible, estos problemas se resolverán en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bc525-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="bc525-117">No se pueden abrir hipervínculos con Internet Explorer11 en Microsoft Windows 8,1 dentro del entorno virtual</span><span class="sxs-lookup"><span data-stu-id="bc525-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="bc525-118">Si intenta abrir hipervínculos desde un entorno virtual, se producirá un error en Windows 8,1 con Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="bc525-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="bc525-119">Esto se debe a que ahora Internet Explorer 11 se incluye con el modo de protección mejorado (EPM) habilitado de forma predeterminada y esto hace que las aplicaciones-V no puedan tener acceso a los objetos de claves de registro, archivos y puertos de comunicaciones obligatorios.</span><span class="sxs-lookup"><span data-stu-id="bc525-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="bc525-120">SOLUCIÓN alternativa: deshabilite EPM en Internet Explorer11 antes de abrir un paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="bc525-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="bc525-121">Esto le permitirá abrir Internet Explorer desde el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="bc525-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="bc525-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc525-122">Related topics</span></span>


[<span data-ttu-id="bc525-123">Acerca de Microsoft Application Virtualization4.6SP3</span><span class="sxs-lookup"><span data-stu-id="bc525-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 





