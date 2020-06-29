---
title: Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming
description: Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817030"
---
# <span data-ttu-id="2d2ba-103">Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="2d2ba-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="2d2ba-104">Para admitir una instalación de App-V más segura, puede usar los procedimientos siguientes para modificar las claves privadas en Windows Server2003 o en Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="2d2ba-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="2d2ba-105">Para modificar los permisos de la clave privada, puede usar la herramienta kit de recursos de Windows Server2003 `WinHttpCertCfg.exe` .</span><span class="sxs-lookup"><span data-stu-id="2d2ba-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="2d2ba-106">Para Windows Server2003, el procedimiento requiere que un certificado que cumpla los requisitos previos enumerados en este documento esté instalado en el equipo o los equipos en los que instalará el servidor de streaming o administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="2d2ba-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="2d2ba-107">Encontrará más información sobre el uso de la `WinHttpCertCfg.exe` herramienta en <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="2d2ba-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="2d2ba-108">En Windows Server2008, el proceso de cambiar las ACL en la clave privada es mucho más simple.</span><span class="sxs-lookup"><span data-stu-id="2d2ba-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="2d2ba-109">La interfaz de usuario del certificado se puede usar para administrar los permisos de clave privada.</span><span class="sxs-lookup"><span data-stu-id="2d2ba-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="2d2ba-110">**Nota:**  El contexto de seguridad predeterminado es servicio de red. sin embargo, en su lugar se puede usar una cuenta de dominio.</span><span class="sxs-lookup"><span data-stu-id="2d2ba-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="2d2ba-111">Para administrar las claves privadas en Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="2d2ba-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="2d2ba-112">En el equipo que se convertirá en el servidor de administración o streaming de App-V, escriba el siguiente comando en un símbolo del sistema para mostrar los permisos actuales asignados a un certificado específico:</span><span class="sxs-lookup"><span data-stu-id="2d2ba-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="2d2ba-113">Si es necesario, modifique los permisos del certificado para proporcionar acceso de lectura al contexto de seguridad que se usará para el servicio de administración o transmisión por secuencias:</span><span class="sxs-lookup"><span data-stu-id="2d2ba-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="2d2ba-114">Compruebe que el contexto de seguridad se haya agregado correctamente mediante una lista de los permisos en el certificado:</span><span class="sxs-lookup"><span data-stu-id="2d2ba-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="2d2ba-115">Para administrar las claves privadas en Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="2d2ba-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="2d2ba-116">Cree una consola de administración de Microsoft (MMC) con el complemento *certificados* que se dirige al almacén de certificados de la *máquina local* .</span><span class="sxs-lookup"><span data-stu-id="2d2ba-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="2d2ba-117">Expanda la consola MMC y seleccione **administrar claves privadas**.</span><span class="sxs-lookup"><span data-stu-id="2d2ba-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="2d2ba-118">En la pestaña **seguridad** , agregue la cuenta **servicio de red** con acceso de **lectura** .</span><span class="sxs-lookup"><span data-stu-id="2d2ba-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="2d2ba-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d2ba-119">Related topics</span></span>


[<span data-ttu-id="2d2ba-120">Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="2d2ba-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="2d2ba-121">Configuración de certificados para admitir streaming seguro</span><span class="sxs-lookup"><span data-stu-id="2d2ba-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 





