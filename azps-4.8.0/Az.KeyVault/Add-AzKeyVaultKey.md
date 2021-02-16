---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: d2c153cf0ae2f5cffbf47656d3ae64a531cb780b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413798"
---
# <span data-ttu-id="d1f01-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="d1f01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f01-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f01-103">키 자격 증명 모음에 키를 생성하거나 키를 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="d1f01-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1f01-104">SYNTAX</span></span>

### <span data-ttu-id="d1f01-105">InteractiveCreate(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1f01-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f01-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="d1f01-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f01-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="d1f01-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f01-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="d1f01-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f01-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="d1f01-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f01-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="d1f01-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1f01-111">설명</span><span class="sxs-lookup"><span data-stu-id="d1f01-111">DESCRIPTION</span></span>
<span data-ttu-id="d1f01-112">**Add-AzKeyVaultKey** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 키를 만들거나 키를 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="d1f01-113">이 cmdlet을 사용하여 다음 방법 중 원하는 방법으로 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="d1f01-114">Key Vault 서비스의 HSM(하드웨어 보안 모듈)에서 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="d1f01-115">Key Vault 서비스에서 소프트웨어에 키를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="d1f01-116">사용자 자신의 HSM(하드웨어 보안 모듈)에서 Key Vault 서비스의 HSM으로 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="d1f01-117">컴퓨터의 .pfx 파일에서 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="d1f01-118">컴퓨터의 .pfx 파일에서 Key Vault 서비스의 HSM(하드웨어 보안 모듈)으로 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="d1f01-119">이러한 작업의 경우 키 특성을 제공하거나 기본 설정을 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="d1f01-120">키 자격 증명 모음의 기존 키와 이름이 같은 키를 만들거나 가져오는 경우 원래 키가 새 키에 대해 지정한 값으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="d1f01-121">해당 버전의 키에 대한 버전별 URI를 사용하여 이전 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="d1f01-122">키 버전 및 URI 구조에 [](http://go.microsoft.com/fwlink/?linkid=518560) 대한 자세한 내용은 Key Vault REST API 설명서의 키 및 비밀 정보를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1f01-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="d1f01-123">참고: 자체 하드웨어 보안 모듈에서 키를 가져오기 위해 먼저 Azure Key Vault BYOK 도구 모음을 사용하여 BYOK 패키지(.byok 파일 이름 확장명을 사용하는 파일)를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="d1f01-124">자세한 내용은 Azure Key Vault에 대한 HSM-Protected 키를 생성하고 [전송하는 방법을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="d1f01-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="d1f01-125">키가 만들어지거나 업데이트된 후 cmdlet을 사용하여 키를 백업하는 Backup-AzKeyVaultKey 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="d1f01-126">삭제되지 않은 기능은 없습니다. 따라서 키를 실수로 삭제하거나 삭제한 다음 마음이 바뀌면 복원할 수 있는 백업이 없는 한 키를 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="d1f01-127">예제</span><span class="sxs-lookup"><span data-stu-id="d1f01-127">EXAMPLES</span></span>

### <span data-ttu-id="d1f01-128">예제 1: 키 만들기</span><span class="sxs-lookup"><span data-stu-id="d1f01-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="d1f01-129">이 명령은 Contoso라는 키 자격 증명 모음에 ITSoftware라는 소프트웨어 보호 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="d1f01-130">예제 2: HSM 보호 키 만들기</span><span class="sxs-lookup"><span data-stu-id="d1f01-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="d1f01-131">이 명령은 Contoso라는 키 자격 증명 모음에 HSM으로 보호된 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="d1f01-132">예제 3: 기본값이 아닌 키 만들기</span><span class="sxs-lookup"><span data-stu-id="d1f01-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="d1f01-133">첫 번째 명령은 암호 해독 값을 저장하고 $KeyOperations 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="d1f01-134">두 번째 명령은 **Get-Date** cmdlet을 사용하여 UTC로 정의된 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="d1f01-135">해당 개체는 향후 2년의 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="d1f01-136">이 명령은 이 날짜를 $Expires 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="d1f01-137">자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="d1f01-138">세 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="d1f01-139">해당 개체는 현재 UTC 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-139">That object specifies current UTC time.</span></span> <span data-ttu-id="d1f01-140">이 명령은 이 날짜를 $NotBefore 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="d1f01-141">마지막 명령은 HSM 보호 키인 ITHsmNonDefault라는 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="d1f01-142">이 명령은 저장된 허용되는 키 작업에 대한 값을 $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="d1f01-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="d1f01-143">이 명령은 이전 명령에서 만든 *Expires* 및 *NotBefore* 매개 변수의 시간 및 높은 심각도 및 IT에 대한 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="d1f01-144">새 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-144">The new key is disabled.</span></span> <span data-ttu-id="d1f01-145">**Set-AzKeyVaultKey** cmdlet을 사용하여 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="d1f01-146">예제 4: HSM 보호 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1f01-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="d1f01-147">이 명령은 *KeyFilePath* 매개 변수가 지정하는 위치에서 ITByok이라는 키를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="d1f01-148">가져온 키는 HSM 보호 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="d1f01-149">자체 하드웨어 보안 모듈에서 키를 가져오기 위해 먼저 Azure Key Vault BYOK 도구 모음을 사용하여 BYOK 패키지(.byok 파일 이름 확장명을 사용하는 파일)를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="d1f01-150">자세한 내용은 Azure Key Vault에 대한 HSM-Protected 키를 생성하고 [전송하는 방법을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="d1f01-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="d1f01-151">예제 5: 소프트웨어로 보호된 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1f01-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="d1f01-152">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="d1f01-153">자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="d1f01-154">두 번째 명령은 Contoso 키 자격 증명 모음에 소프트웨어 암호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="d1f01-155">이 명령은 키의 위치와 키에 저장된 암호를 $Password.</span><span class="sxs-lookup"><span data-stu-id="d1f01-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="d1f01-156">예제 6: 키 가져오기 및 특성 할당</span><span class="sxs-lookup"><span data-stu-id="d1f01-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="d1f01-157">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="d1f01-158">두 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만든 다음 해당 개체를 $Expires 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="d1f01-159">세 번째 명령은 심각도 $tags 및 IT에 대한 태그를 설정하는 $tags 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="d1f01-160">마지막 명령은 지정된 위치에서 키를 HSM 키로 가져오습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="d1f01-161">이 명령은 $Expires 저장된 만료 시간 및 $Password 저장한 태그를 $tags.</span><span class="sxs-lookup"><span data-stu-id="d1f01-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="d1f01-162">예제 7: "BYOK(Bring Your Own Key) 기능"에 대한 KEK(키 교환 키) 생성</span><span class="sxs-lookup"><span data-stu-id="d1f01-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="d1f01-163">키(KEK(키 교환 키)라고도 하는 키)를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="d1f01-164">KEK는 가져오기 키 작업만 있는 RSA-HSM 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="d1f01-165">Key Vault 프리미엄 SKU만 RSA-HSM 키를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="d1f01-166">자세한 내용은 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="d1f01-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="d1f01-167">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f01-167">PARAMETERS</span></span>

### <span data-ttu-id="d1f01-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f01-168">-DefaultProfile</span></span>
<span data-ttu-id="d1f01-169">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d1f01-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1f01-170">-Destination</span><span class="sxs-lookup"><span data-stu-id="d1f01-170">-Destination</span></span>
<span data-ttu-id="d1f01-171">Key Vault 서비스에서 소프트웨어 보호 키 또는 HSM 보호 키로 키를 추가할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="d1f01-172">유효한 값은 HSM 및 Software입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="d1f01-173">참고: HSM을 대상으로 사용하려면 HSM을 지원하는 키 자격 증명 모음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="d1f01-174">Azure Key Vault의 서비스 계층 및 기능에 대한 자세한 내용은 Azure Key Vault 가격 책정 웹 사이트를 [참조하세요.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="d1f01-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="d1f01-175">이 매개 변수는 새 키를 만들 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="d1f01-176">*KeyFilePath* 매개 변수를 사용하여 키를 가져오는 경우 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="d1f01-177">이 매개 변수를 지정하지 않으면 이 cmdlet은 .byok 파일 이름 확장명을 사용하는 키를 가져오면 해당 키를 HSM 보호 키로 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="d1f01-178">cmdlet은 소프트웨어 보호 키로 이 키를 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="d1f01-179">이 매개 변수를 지정하지 않으면 이 cmdlet은 .pfx 파일 이름 확장명을 사용하는 키를 가져오면 소프트웨어 보호 키로 키를 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="d1f01-180">-Disable</span><span class="sxs-lookup"><span data-stu-id="d1f01-180">-Disable</span></span>
<span data-ttu-id="d1f01-181">추가하는 키가 초기 비활성화 상태로 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="d1f01-182">키를 사용하려는 시도는 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="d1f01-183">나중에 사용하도록 설정하려는 키를 미리 로드하는 경우 이 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="d1f01-184">-Expires</span><span class="sxs-lookup"><span data-stu-id="d1f01-184">-Expires</span></span>
<span data-ttu-id="d1f01-185">이 cmdlet에서 추가하는 키에 대한 만료 시간을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="d1f01-186">이 매개 변수는 UTC(협정 세계시)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d1f01-187">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="d1f01-188">자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="d1f01-189">이 매개 변수를 지정하지 않으면 키가 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-189">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="d1f01-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1f01-190">-InputObject</span></span>
<span data-ttu-id="d1f01-191">자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-191">Vault object.</span></span>

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

### <span data-ttu-id="d1f01-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="d1f01-192">-KeyFilePassword</span></span>
<span data-ttu-id="d1f01-193">가져온 파일의 암호를 **SecureString** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="d1f01-194">**SecureString** 개체를 얻습니다. **ConvertTo-SecureString** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="d1f01-195">자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="d1f01-196">.pfx 파일 이름 확장명을 사용하여 파일을 가져오기 위해 이 암호를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f01-197">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="d1f01-197">-KeyFilePath</span></span>
<span data-ttu-id="d1f01-198">이 cmdlet에서 가져오는 키 자료를 포함하는 로컬 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="d1f01-199">유효한 파일 이름 확장명은 .byok 및 .pfx입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="d1f01-200">파일이 .byok 파일인 경우 키는 가져오기 후에 HSM에 의해 자동으로 보호되며 이 기본값을 다시 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="d1f01-201">파일이 .pfx 파일인 경우 키를 가져온 후 소프트웨어에 의해 자동으로 보호됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="d1f01-202">이 기본값을 오버라이드하기  위해 키가 HSM으로 보호되지 있도록 대상 매개 변수를 HSM으로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="d1f01-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="d1f01-203">이 매개 변수를 지정하는 경우 *대상* 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f01-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="d1f01-204">-KeyOps</span></span>
<span data-ttu-id="d1f01-205">이 cmdlet에서 추가하는 키를 사용하여 수행할 수 있는 작업의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="d1f01-206">이 매개 변수를 지정하지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="d1f01-207">이 매개 변수에 허용되는 값은 [JWK(JSON 웹 키)](http://go.microsoft.com/fwlink/?LinkID=613300)사양에 정의된 키 작업의 콤마로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="d1f01-208">encrypt</span><span class="sxs-lookup"><span data-stu-id="d1f01-208">encrypt</span></span>
- <span data-ttu-id="d1f01-209">암호 해독</span><span class="sxs-lookup"><span data-stu-id="d1f01-209">decrypt</span></span>
- <span data-ttu-id="d1f01-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-210">wrapKey</span></span>
- <span data-ttu-id="d1f01-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-211">unwrapKey</span></span>
- <span data-ttu-id="d1f01-212">sign</span><span class="sxs-lookup"><span data-stu-id="d1f01-212">sign</span></span>
- <span data-ttu-id="d1f01-213">확인</span><span class="sxs-lookup"><span data-stu-id="d1f01-213">verify</span></span>
- <span data-ttu-id="d1f01-214">가져오기(KEK에만 해당, 예제 7 참조)</span><span class="sxs-lookup"><span data-stu-id="d1f01-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="d1f01-215">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f01-215">-Name</span></span>
<span data-ttu-id="d1f01-216">키 자격 증명 모음에 추가할 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="d1f01-217">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 키의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="d1f01-218">이름은 길이가 1~63자인 문자열로, 0-9, a-z, A-Z 및 -(대시 기호)만 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="d1f01-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="d1f01-219">-NotBefore</span></span>
<span data-ttu-id="d1f01-220">키를 사용할 수 없는 **시간(DateTime** 개체)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="d1f01-221">이 매개 변수는 UTC를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-221">This parameter uses UTC.</span></span> <span data-ttu-id="d1f01-222">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="d1f01-223">이 매개 변수를 지정하지 않으면 키를 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-223">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="d1f01-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f01-224">-ResourceId</span></span>
<span data-ttu-id="d1f01-225">자격 증명 모음 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-225">Vault Resource Id.</span></span>

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

### <span data-ttu-id="d1f01-226">-Size</span><span class="sxs-lookup"><span data-stu-id="d1f01-226">-Size</span></span>
<span data-ttu-id="d1f01-227">RSA 키 크기(비트)입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-227">RSA key size, in bits.</span></span> <span data-ttu-id="d1f01-228">지정하지 않으면 서비스는 안전한 기본값을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-228">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f01-229">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1f01-229">-Tag</span></span>
<span data-ttu-id="d1f01-230">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d1f01-231">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d1f01-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d1f01-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d1f01-232">-VaultName</span></span>
<span data-ttu-id="d1f01-233">이 cmdlet에서 키를 추가하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="d1f01-234">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="d1f01-235">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f01-235">-Confirm</span></span>
<span data-ttu-id="d1f01-236">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f01-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f01-237">-WhatIf</span></span>
<span data-ttu-id="d1f01-238">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d1f01-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f01-239">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f01-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f01-240">CommonParameters</span></span>
<span data-ttu-id="d1f01-241">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f01-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f01-242">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1f01-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f01-243">입력</span><span class="sxs-lookup"><span data-stu-id="d1f01-243">INPUTS</span></span>

### <span data-ttu-id="d1f01-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d1f01-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d1f01-245">System.String</span><span class="sxs-lookup"><span data-stu-id="d1f01-245">System.String</span></span>

## <span data-ttu-id="d1f01-246">출력</span><span class="sxs-lookup"><span data-stu-id="d1f01-246">OUTPUTS</span></span>

### <span data-ttu-id="d1f01-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="d1f01-248">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1f01-248">NOTES</span></span>

## <span data-ttu-id="d1f01-249">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1f01-249">RELATED LINKS</span></span>

[<span data-ttu-id="d1f01-250">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="d1f01-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="d1f01-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1f01-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

