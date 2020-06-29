---
title: Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo
description: Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817911"
---
# <span data-ttu-id="470f7-103">Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="470f7-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="470f7-104">El método abreviado y la Directiva de publicación de Asociación de tipo de archivo (FTA) está definido y controlado por el archivo XML de publicación, que un servidor de publicación envía a los clientes durante una operación de actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="470f7-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="470f7-105">Cuando el cliente recibe esta información, agrega los datos recién publicados sobre aplicaciones, como iconos y FTAs.</span><span class="sxs-lookup"><span data-stu-id="470f7-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="470f7-106">A continuación, elimina los datos de publicación que no estén actualizados.</span><span class="sxs-lookup"><span data-stu-id="470f7-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="470f7-107">En la versión 4,6 de App-V, se han definido dos valores de clave del registro para permitir a los administradores controlar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="470f7-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="470f7-108">De forma predeterminada, los accesos directos que se crean de forma local mediante la consola del cliente se conservan.</span><span class="sxs-lookup"><span data-stu-id="470f7-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="470f7-109">Cómo cambiar el comportamiento de los métodos abreviados y FTA</span><span class="sxs-lookup"><span data-stu-id="470f7-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="470f7-110">Se han definido dos nuevos valores de registro DWORD para la clave del registro de configuración del cliente, "FileTypePolicy" y "ShortcutPolicy".</span><span class="sxs-lookup"><span data-stu-id="470f7-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="470f7-111">Estos valores de registro DWORD no están presentes de forma predeterminada, pero pueden agregarse de forma manual.</span><span class="sxs-lookup"><span data-stu-id="470f7-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="470f7-112">La clave del registro de configuración se encuentra en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="470f7-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="470f7-113">Hay cuatro valores de directiva definidos en la tabla siguiente y se aplican a ambos valores de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="470f7-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="470f7-114">En la siguiente lista se muestran los valores numéricos de la configuración del registro y el comportamiento aplicado a los tipos de archivo o los accesos directos en una operación de actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="470f7-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470f7-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="470f7-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="470f7-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-117">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="470f7-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="470f7-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="470f7-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="470f7-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="470f7-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-121">Valor predeterminado = 0X2 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="470f7-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-122">(0X0): "ClientOnly": quitar los elementos existentes de la misma fuente de información de publicación y mantener solo los elementos agregados de forma local</span><span class="sxs-lookup"><span data-stu-id="470f7-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="470f7-123">(0x1)-"ServerOnly"-quitar los elementos anticuados de la misma fuente de información de publicación y los elementos que se agreguen de forma local, y agregar los nuevos elementos</span><span class="sxs-lookup"><span data-stu-id="470f7-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="470f7-124">(0X2): "ClientAndServer"-quitar los elementos anticuados de la misma fuente de información de publicación, mantener los elementos agregados localmente y agregar los nuevos elementos (valor predeterminado si no están presentes en App-V 4,6).</span><span class="sxs-lookup"><span data-stu-id="470f7-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="470f7-125">(0X3): "nochange"-no realizar cambios en los tipos de archivo ni en los accesos directos</span><span class="sxs-lookup"><span data-stu-id="470f7-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="470f7-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="470f7-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="470f7-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-128">Valor predeterminado = 0X2</span><span class="sxs-lookup"><span data-stu-id="470f7-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="470f7-129">(0X0): "ClientOnly": quitar los elementos existentes de la misma fuente de información de publicación y mantener solo los elementos agregados localmente</span><span class="sxs-lookup"><span data-stu-id="470f7-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="470f7-130">(0x1)-"ServerOnly"-quitar los elementos anticuados de la misma fuente de información de publicación y los elementos agregados localmente, y agregar los nuevos elementos</span><span class="sxs-lookup"><span data-stu-id="470f7-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="470f7-131">(0X2): "ClientAndServer"-quitar los elementos anticuados de la misma fuente de información de publicación, mantener los elementos agregados localmente y agregar los nuevos elementos (valor predeterminado si no hay ninguno)</span><span class="sxs-lookup"><span data-stu-id="470f7-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="470f7-132">(0X3): "nochange"-no realizar cambios en los tipos de archivo ni en los accesos directos</span><span class="sxs-lookup"><span data-stu-id="470f7-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="470f7-133">**Nota:**  Los valores de texto hacen referencia a los valores de los atributos XML en el archivo XML de publicación.</span><span class="sxs-lookup"><span data-stu-id="470f7-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="470f7-134">Puede establecer estos valores manualmente si ha implementado una solución de publicación HTTP personalizada.</span><span class="sxs-lookup"><span data-stu-id="470f7-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





