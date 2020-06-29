---
title: Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell
description: Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell
author: dansimp
ms.assetid: 2be6fb72-f3a6-4550-bba1-6defa78ca08a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39651df4d62971e39c4228ffce665386d5c9769d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814038"
---
# <span data-ttu-id="d393d-103">Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="d393d-103">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span>

<span data-ttu-id="d393d-104">Use el siguiente procedimiento de PowerShell para convertir cualquier número de cuentas de usuario o de equipo de servicios de dominio de Active Directory (AD DS) en identificadores de seguridad (SID) con formato en el formato estándar y en el formato hexadecimal utilizado por Microsoft SQL Server cuando se ejecuten scripts SQL.</span><span class="sxs-lookup"><span data-stu-id="d393d-104">Use the following PowerShell procedure to convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by Microsoft SQL Server when running SQL scripts.</span></span>

<span data-ttu-id="d393d-105">Antes de intentar este procedimiento, debe leer y comprender la información y los ejemplos que se muestran en la siguiente lista:</span><span class="sxs-lookup"><span data-stu-id="d393d-105">Before attempting this procedure, you should read and understand the information and examples displayed in the following list:</span></span>

- <span data-ttu-id="d393d-106">**. ENTRADAS** : cuenta o cuentas que se usan para convertir al formato de SID.</span><span class="sxs-lookup"><span data-stu-id="d393d-106">**.INPUTS** – The account or accounts used to convert to SID format.</span></span> <span data-ttu-id="d393d-107">Puede ser un nombre de cuenta único o una matriz de nombres de cuenta.</span><span class="sxs-lookup"><span data-stu-id="d393d-107">This can be a single account name or an array of account names.</span></span>

- <span data-ttu-id="d393d-108">**. RESULTADOS** : una lista de nombres de cuenta con el SID correspondiente en formato estándar y hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d393d-108">**.OUTPUTS** - A list of account names with the corresponding SID in standard and hexadecimal formats.</span></span>

- <span data-ttu-id="d393d-109">**Acerca** -</span><span class="sxs-lookup"><span data-stu-id="d393d-109">**Examples** -</span></span>

    <span data-ttu-id="d393d-110">**.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-List**.</span><span class="sxs-lookup"><span data-stu-id="d393d-110">**.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List**.</span></span>

    **<span data-ttu-id="d393d-111">$accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "dominio \ _user \ _account2")</span><span class="sxs-lookup"><span data-stu-id="d393d-111">$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")</span></span>**

    **<span data-ttu-id="d393d-112">.\\ConvertToSID.ps1 $accountsArray | Write-Output-FilePath .\\SIDs.txt-width 200</span><span class="sxs-lookup"><span data-stu-id="d393d-112">.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200</span></span>**

## <span data-ttu-id="d393d-113">Para convertir cualquier número de cuentas de usuario o de equipo de servicios de dominio de Active Directory (AD DS) en identificadores de seguridad con formato (SID)</span><span class="sxs-lookup"><span data-stu-id="d393d-113">To convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs)</span></span>

1. <span data-ttu-id="d393d-114">Copie el script siguiente en un editor de texto y guárdelo como un archivo de script de PowerShell, por ejemplo **ConvertToSIDs.ps1**.</span><span class="sxs-lookup"><span data-stu-id="d393d-114">Copy the following script into a text editor and save it as a PowerShell script file, for example **ConvertToSIDs.ps1**.</span></span>
1. <span data-ttu-id="d393d-115">Para abrir una consola de PowerShell, haga clic en **iniciar** y escriba **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="d393d-115">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="d393d-116">Haga clic con el botón derecho en **Windows PowerShell** y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="d393d-116">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

   ```powershell
   <#
   .SYNOPSIS
   This PowerShell script will take an array of account names and try to convert each of them to the corresponding SID in standard and hexadecimal formats.
   .DESCRIPTION
   This is a PowerShell script that converts any number of Active Directory (AD) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by SQL server when running SQL scripts.
   .INPUTS
   The account(s) to convert to SID format. This can be a single account name or an array of account names. Please see examples below.
   .OUTPUTS
   A list of account names with the corresponding SID in standard and hexadecimal formats
   .EXAMPLE
   .\ConvertToSID.ps1 DOMAIN\user_account1 DOMAIN\machine_account1$ DOMAIN\user_account2 | Format-List
   .EXAMPLE
   $accountsArray = @("DOMAIN\user_account1", "DOMAIN\machine_account1$", "DOMAIN_user_account2")
   .\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\SIDs.txt -Width 200
   #>

   function ConvertSIDToHexFormat
   {

      param([System.Security.Principal.SecurityIdentifier]$sidToConvert)

      $sb = New-Object System.Text.StringBuilder
      [int] $binLength = $sidToConvert.BinaryLength
      [Byte[]] $byteArray = New-Object Byte[] $binLength
      $sidToConvert.GetBinaryForm($byteArray, 0)
      foreach($byte in $byteArray)
      {
          $sb.Append($byte.ToString("X2")) |Out-Null
      }
      return $sb.ToString()
   }
    [string[]]$myArgs = $args
   if(($myArgs.Length -lt 1) -or ($myArgs[0].CompareTo("/?") -eq 0))
   {

    [string]::Format("{0}====== Description ======{0}{0}" +
                  "  Converts any number of user or machine account names to string and hexadecimal SIDs.{0}" +
                  "  Pass the account(s) as space separated command line parameters. (For example 'ConvertToSID.ps1 DOMAIN\Account1 DOMAIN\Account2 ...'){0}" +
                  "  The output is written to the console in the format 'Account name    SID as string   SID as hexadecimal'{0}" +
                  "  And can be written out to a file using standard PowerShell redirection{0}" +
                  "  Please specify user accounts in the format 'DOMAIN\username'{0}" +
                  "  Please specify machine accounts in the format 'DOMAIN\machinename$'{0}" +
                  "  For more help content, please run 'Get-Help ConvertToSID.ps1'{0}" +
                  "{0}====== Arguments ======{0}" +
                  "{0}  /?    Show this help message", [Environment]::NewLine)
   }
   else
   {
       #If an array was passed in, try to split it
       if($myArgs.Length -eq 1)
       {
           $myArgs = $myArgs.Split(' ')
       }

       #Parse the arguments for account names
       foreach($accountName in $myArgs)
       {
           [string[]] $splitString = $accountName.Split('\')  # We're looking for the format "DOMAIN\Account" so anything that does not match, we reject
           if($splitString.Length -ne 2)
           {
               $message = [string]::Format("{0} is not a valid account name. Expected format 'Domain\username' for user accounts or 'DOMAIN\machinename$' for machine accounts.", $accountName)
               Write-Error -Message $message
               continue
           }

           #Convert any account names to SIDs
           try
           {
               [System.Security.Principal.NTAccount] $account = New-Object System.Security.Principal.NTAccount($splitString[0], $splitString[1])
               [System.Security.Principal.SecurityIdentifier] $SID = [System.Security.Principal.SecurityIdentifier]($account.Translate([System.Security.Principal.SecurityIdentifier]))
           }
           catch [System.Security.Principal.IdentityNotMappedException]
           {
               $message = [string]::Format("Failed to translate account object '{0}' to a SID. Please verify that this is a valid user or machine account.", $account.ToString())
               Write-Error -Message $message
               continue
           }

           #Convert regular SID to binary format used by SQL
           $hexSIDString = ConvertSIDToHexFormat $SID

           $SIDs = New-Object PSObject
           $SIDs | Add-Member NoteProperty Account $accountName
           $SIDs | Add-Member NoteProperty SID $SID.ToString()
           $SIDs | Add-Member NoteProperty Hexadecimal $hexSIDString

           Write-Output $SIDs
       }
   }
   ```

1. <span data-ttu-id="d393d-117">Ejecute el script que guardó en el paso uno de este procedimiento y pase las cuentas para convertirlas como argumentos.</span><span class="sxs-lookup"><span data-stu-id="d393d-117">Run the script you saved in step one of this procedure passing the accounts to convert as arguments.</span></span>

   <span data-ttu-id="d393d-118">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d393d-118">For example,</span></span>

   **<span data-ttu-id="d393d-119">.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-List</span><span class="sxs-lookup"><span data-stu-id="d393d-119">.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List</span></span>**
   
   <span data-ttu-id="d393d-120">o</span><span class="sxs-lookup"><span data-stu-id="d393d-120">or</span></span>
   
   <span data-ttu-id="d393d-121">**$accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "dominio \ _user \ _account2")** 
    **.\\ConvertToSID.ps1 $accountsArray | Write-Output-FilePath .\\SIDs.txt-width 200**</span><span class="sxs-lookup"><span data-stu-id="d393d-121">**$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")**
 **.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200**</span></span>

**<span data-ttu-id="d393d-122">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="d393d-122">Got an App-V issue?</span></span>** <span data-ttu-id="d393d-123">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d393d-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d393d-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d393d-124">Related topics</span></span>

[<span data-ttu-id="d393d-125">Administrar 5.1 de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="d393d-125">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)
