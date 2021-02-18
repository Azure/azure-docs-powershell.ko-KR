---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 61125ae7d9fa78ec9f121cc9b60610258ad2c67c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405400"
---
# <span data-ttu-id="1e405-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e405-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="1e405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e405-102">SYNOPSIS</span></span>
<span data-ttu-id="1e405-103">키 자격 증명 모음에 키를 생성하거나 키를 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="1e405-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e405-104">SYNTAX</span></span>

### <span data-ttu-id="1e405-105">InteractiveCreate(기본값)</span><span class="sxs-lookup"><span data-stu-id="1e405-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="1e405-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="1e405-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="1e405-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="1e405-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="1e405-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="1e405-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="1e405-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e405-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="1e405-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="1e405-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="1e405-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e405-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="1e405-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e405-117">설명</span><span class="sxs-lookup"><span data-stu-id="1e405-117">DESCRIPTION</span></span>
<span data-ttu-id="1e405-118">**Add-AzKeyVaultKey** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 키를 만들거나 키를 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="1e405-119">이 cmdlet을 사용하여 다음 방법 중 원하는 방법으로 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="1e405-120">Key Vault 서비스의 HSM(하드웨어 보안 모듈)에서 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="1e405-121">Key Vault 서비스에서 소프트웨어에 키를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="1e405-122">사용자 자신의 HSM(하드웨어 보안 모듈)에서 Key Vault 서비스의 HSM으로 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="1e405-123">컴퓨터의 .pfx 파일에서 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="1e405-124">컴퓨터의 .pfx 파일에서 Key Vault 서비스의 HSM(하드웨어 보안 모듈)으로 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="1e405-125">이러한 작업의 경우 키 특성을 제공하거나 기본 설정을 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="1e405-126">키 자격 증명 모음의 기존 키와 이름이 같은 키를 만들거나 가져오는 경우 원래 키가 새 키에 대해 지정한 값으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="1e405-127">해당 버전의 키에 대한 버전별 URI를 사용하여 이전 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="1e405-128">키 버전 및 URI 구조에 [](http://go.microsoft.com/fwlink/?linkid=518560) 대한 자세한 내용은 Key Vault REST API 설명서의 키 및 비밀 정보를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1e405-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="1e405-129">참고: 자체 하드웨어 보안 모듈에서 키를 가져오기 위해 먼저 Azure Key Vault BYOK 도구 모음을 사용하여 BYOK 패키지(.byok 파일 이름 확장명을 사용하는 파일)를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="1e405-130">자세한 내용은 Azure Key Vault에 대한 HSM-Protected 키를 생성하고 [전송하는 방법을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="1e405-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="1e405-131">키가 만들어지거나 업데이트된 후 cmdlet을 사용하여 키를 백업하는 Backup-AzKeyVaultKey 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="1e405-132">삭제되지 않은 기능은 없습니다. 따라서 키를 실수로 삭제하거나 삭제한 다음 마음이 바뀌면 복원할 수 있는 백업이 없는 한 키를 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="1e405-133">예제</span><span class="sxs-lookup"><span data-stu-id="1e405-133">EXAMPLES</span></span>

### <span data-ttu-id="1e405-134">예제 1: 키 만들기</span><span class="sxs-lookup"><span data-stu-id="1e405-134">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e405-135">이 명령은 Contoso라는 키 자격 증명 모음에 ITSoftware라는 소프트웨어 보호 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e405-136">예제 2: HSM 보호 키 만들기</span><span class="sxs-lookup"><span data-stu-id="1e405-136">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e405-137">이 명령은 Contoso라는 키 자격 증명 모음에 HSM으로 보호된 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e405-138">예제 3: 기본값이 아닌 키 만들기</span><span class="sxs-lookup"><span data-stu-id="1e405-138">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="1e405-139">첫 번째 명령은 암호 해독 값을 저장하고 $KeyOperations 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="1e405-140">두 번째 명령은 **Get-Date** cmdlet을 사용하여 UTC로 정의된 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="1e405-141">해당 개체는 향후 2년의 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="1e405-142">이 명령은 이 날짜를 $Expires 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="1e405-143">자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1e405-144">세 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e405-145">해당 개체는 현재 UTC 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-145">That object specifies current UTC time.</span></span> <span data-ttu-id="1e405-146">이 명령은 이 날짜를 $NotBefore 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="1e405-147">마지막 명령은 HSM 보호 키인 ITHsmNonDefault라는 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="1e405-148">이 명령은 저장된 허용되는 키 작업에 대한 값을 $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="1e405-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="1e405-149">이 명령은 이전 명령에서 만든 *Expires* 및 *NotBefore* 매개 변수의 시간 및 높은 심각도 및 IT에 대한 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="1e405-150">새 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-150">The new key is disabled.</span></span> <span data-ttu-id="1e405-151">**Set-AzKeyVaultKey** cmdlet을 사용하여 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="1e405-152">예제 4: HSM 보호 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e405-152">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e405-153">이 명령은 *KeyFilePath* 매개 변수가 지정하는 위치에서 ITByok이라는 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="1e405-154">가져온 키는 HSM 보호 키입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="1e405-155">자체 하드웨어 보안 모듈에서 키를 가져오기 위해 먼저 Azure Key Vault BYOK 도구 모음을 사용하여 BYOK 패키지(.byok 파일 이름 확장명을 사용하는 파일)를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="1e405-156">자세한 내용은 Azure Key Vault에 대한 HSM-Protected 키를 생성하고 [전송하는 방법을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="1e405-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="1e405-157">예제 5: 소프트웨어로 보호된 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e405-157">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e405-158">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="1e405-159">자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1e405-160">두 번째 명령은 Contoso 키 자격 증명 모음에 소프트웨어 암호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="1e405-161">이 명령은 키의 위치와 키에 저장된 암호를 $Password.</span><span class="sxs-lookup"><span data-stu-id="1e405-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="1e405-162">예제 6: 키 가져오기 및 특성 할당</span><span class="sxs-lookup"><span data-stu-id="1e405-162">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="1e405-163">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="1e405-164">두 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만든 다음 해당 개체를 $Expires 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="1e405-165">세 번째 명령은 심각도 $tags 및 IT에 대한 태그를 설정하는 $tags 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="1e405-166">마지막 명령은 지정된 위치에서 키를 HSM 키로 가져오습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="1e405-167">이 명령은 $Expires 저장된 만료 시간 및 $Password 저장한 태그를 $tags.</span><span class="sxs-lookup"><span data-stu-id="1e405-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="1e405-168">예제 7: "BYOK(Bring Your Own Key) 기능"에 대한 KEK(키 교환 키) 생성</span><span class="sxs-lookup"><span data-stu-id="1e405-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="1e405-169">키(KEK(키 교환 키)라고도 하는 키)를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="1e405-170">KEK는 가져오기 키 작업만 있는 RSA-HSM 키입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="1e405-171">Key Vault 프리미엄 SKU만 RSA-HSM 키를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="1e405-172">자세한 내용은 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="1e405-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="1e405-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e405-173">PARAMETERS</span></span>

### <span data-ttu-id="1e405-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="1e405-174">-CurveName</span></span>
<span data-ttu-id="1e405-175">타원 곡선 암호화의 곡선 이름을 지정합니다. 이 값은 KeyType이 EC일 때 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e405-176">-DefaultProfile</span></span>
<span data-ttu-id="1e405-177">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1e405-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-178">-Destination</span><span class="sxs-lookup"><span data-stu-id="1e405-178">-Destination</span></span>
<span data-ttu-id="1e405-179">Key Vault 서비스에서 소프트웨어 보호 키 또는 HSM 보호 키로 키를 추가할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="1e405-180">유효한 값은 HSM 및 Software입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="1e405-181">참고: HSM을 대상으로 사용하려면 HSM을 지원하는 키 자격 증명 모음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="1e405-182">Azure Key Vault의 서비스 계층 및 기능에 대한 자세한 내용은 Azure Key Vault 가격 책정 웹 사이트를 [참조하세요.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="1e405-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="1e405-183">이 매개 변수는 새 키를 만들 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="1e405-184">*KeyFilePath* 매개 변수를 사용하여 키를 가져오는 경우 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="1e405-185">이 매개 변수를 지정하지 않으면 이 cmdlet은 .byok 파일 이름 확장명을 사용하는 키를 가져오면 해당 키를 HSM 보호 키로 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="1e405-186">cmdlet은 소프트웨어 보호 키로 이 키를 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="1e405-187">이 매개 변수를 지정하지 않으면 이 cmdlet은 .pfx 파일 이름 확장명을 사용하는 키를 가져오면 소프트웨어 보호 키로 키를 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-188">-Disable</span><span class="sxs-lookup"><span data-stu-id="1e405-188">-Disable</span></span>
<span data-ttu-id="1e405-189">추가하는 키가 초기 비활성화 상태로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="1e405-190">키를 사용하려는 시도는 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="1e405-191">나중에 사용하도록 설정하려는 키를 미리 로드하는 경우 이 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-192">-Expires</span><span class="sxs-lookup"><span data-stu-id="1e405-192">-Expires</span></span>
<span data-ttu-id="1e405-193">이 cmdlet에서 추가하는 키에 대한 만료 시간을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="1e405-194">이 매개 변수는 UTC(협정 세계시)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1e405-195">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e405-196">자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="1e405-197">이 매개 변수를 지정하지 않으면 키가 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-197">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1e405-198">-HsmName</span></span>
<span data-ttu-id="1e405-199">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-199">HSM name.</span></span> <span data-ttu-id="1e405-200">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="1e405-201">-HsmObject</span></span>
<span data-ttu-id="1e405-202">HSM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="1e405-203">-HsmResourceId</span></span>
<span data-ttu-id="1e405-204">HSM의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e405-205">-InputObject</span></span>
<span data-ttu-id="1e405-206">자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-206">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="1e405-207">-KeyFilePassword</span></span>
<span data-ttu-id="1e405-208">가져온 파일의 암호를 **SecureString** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="1e405-209">**SecureString** 개체를 얻습니다. **ConvertTo-SecureString** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="1e405-210">자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="1e405-211">.pfx 파일 이름 확장명을 사용하여 파일을 가져오기 위해 이 암호를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="1e405-212">-KeyFilePath</span></span>
<span data-ttu-id="1e405-213">이 cmdlet에서 가져오는 키 자료를 포함하는 로컬 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="1e405-214">유효한 파일 이름 확장명은 .byok 및 .pfx입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="1e405-215">파일이 .byok 파일인 경우 키는 가져오기 후에 HSM에 의해 자동으로 보호되며 이 기본값을 다시 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="1e405-216">파일이 .pfx 파일인 경우 키를 가져온 후 소프트웨어에 의해 자동으로 보호됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="1e405-217">이 기본값을 오버라이드하기  위해 키가 HSM으로 보호되지 있도록 대상 매개 변수를 HSM으로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="1e405-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="1e405-218">이 매개 변수를 지정하는 경우 *대상* 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="1e405-219">-KeyOps</span></span>
<span data-ttu-id="1e405-220">이 cmdlet에서 추가하는 키를 사용하여 수행할 수 있는 작업의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="1e405-221">이 매개 변수를 지정하지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="1e405-222">이 매개 변수에 허용되는 값은 [JWK(JSON 웹 키)](http://go.microsoft.com/fwlink/?LinkID=613300)사양에 정의된 키 작업의 콤마로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="1e405-223">encrypt</span><span class="sxs-lookup"><span data-stu-id="1e405-223">encrypt</span></span>
- <span data-ttu-id="1e405-224">암호 해독</span><span class="sxs-lookup"><span data-stu-id="1e405-224">decrypt</span></span>
- <span data-ttu-id="1e405-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="1e405-225">wrapKey</span></span>
- <span data-ttu-id="1e405-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="1e405-226">unwrapKey</span></span>
- <span data-ttu-id="1e405-227">sign</span><span class="sxs-lookup"><span data-stu-id="1e405-227">sign</span></span>
- <span data-ttu-id="1e405-228">확인</span><span class="sxs-lookup"><span data-stu-id="1e405-228">verify</span></span>
- <span data-ttu-id="1e405-229">가져오기(KEK에만 해당, 예제 7 참조)</span><span class="sxs-lookup"><span data-stu-id="1e405-229">import (for KEK only, see example 7)</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1e405-230">-KeyType</span></span>
<span data-ttu-id="1e405-231">이 키의 키 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-231">Specifies the key type of this key.</span></span> <span data-ttu-id="1e405-232">BYOK 키를 가져올 때 기본값은 'RSA'입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-232">When importing BYOK keys, it defaults to 'RSA'.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-233">-Name</span><span class="sxs-lookup"><span data-stu-id="1e405-233">-Name</span></span>
<span data-ttu-id="1e405-234">키 자격 증명 모음에 추가할 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-234">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="1e405-235">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 키의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-235">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="1e405-236">이름은 길이가 1~63자인 문자열로, 0-9, a-z, A-Z 및 -(대시 기호)만 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-236">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-237">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1e405-237">-NotBefore</span></span>
<span data-ttu-id="1e405-238">키를 사용할 수 없는 **시간(DateTime** 개체)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-238">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="1e405-239">이 매개 변수는 UTC를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-239">This parameter uses UTC.</span></span> <span data-ttu-id="1e405-240">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-240">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e405-241">이 매개 변수를 지정하지 않으면 키를 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-241">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-242">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e405-242">-ResourceId</span></span>
<span data-ttu-id="1e405-243">자격 증명 모음 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-243">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-244">-Size</span><span class="sxs-lookup"><span data-stu-id="1e405-244">-Size</span></span>
<span data-ttu-id="1e405-245">RSA 키 크기(비트)입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-245">RSA key size, in bits.</span></span> <span data-ttu-id="1e405-246">지정하지 않으면 서비스는 안전한 기본값을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-246">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-247">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e405-247">-Tag</span></span>
<span data-ttu-id="1e405-248">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-248">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e405-249">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1e405-249">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-250">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e405-250">-VaultName</span></span>
<span data-ttu-id="1e405-251">이 cmdlet에서 키를 추가하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-251">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="1e405-252">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-252">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-253">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e405-253">-Confirm</span></span>
<span data-ttu-id="1e405-254">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-254">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e405-255">-WhatIf</span></span>
<span data-ttu-id="1e405-256">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1e405-256">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e405-257">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-257">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e405-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e405-258">CommonParameters</span></span>
<span data-ttu-id="1e405-259">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e405-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e405-260">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e405-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e405-261">입력</span><span class="sxs-lookup"><span data-stu-id="1e405-261">INPUTS</span></span>

### <span data-ttu-id="1e405-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1e405-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1e405-263">System.String</span><span class="sxs-lookup"><span data-stu-id="1e405-263">System.String</span></span>

## <span data-ttu-id="1e405-264">출력</span><span class="sxs-lookup"><span data-stu-id="1e405-264">OUTPUTS</span></span>

### <span data-ttu-id="1e405-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e405-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1e405-266">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e405-266">NOTES</span></span>

## <span data-ttu-id="1e405-267">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e405-267">RELATED LINKS</span></span>

[<span data-ttu-id="1e405-268">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e405-268">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="1e405-269">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e405-269">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="1e405-270">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e405-270">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

