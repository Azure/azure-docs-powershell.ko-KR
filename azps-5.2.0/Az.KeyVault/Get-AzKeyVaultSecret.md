---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 18b87f6a83f335958e9c10e392d859ae307e9e87
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361698"
---
# <span data-ttu-id="e7b77-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e7b77-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="e7b77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b77-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b77-103">키 자격 증명 모음에서 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="e7b77-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7b77-104">SYNTAX</span></span>

### <span data-ttu-id="e7b77-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e7b77-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="e7b77-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="e7b77-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="e7b77-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="e7b77-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="e7b77-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="e7b77-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="e7b77-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b77-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="e7b77-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7b77-114">설명</span><span class="sxs-lookup"><span data-stu-id="e7b77-114">DESCRIPTION</span></span>
<span data-ttu-id="e7b77-115">**Get-AzKeyVaultSecret** cmdlet은 키 자격 증명 모음에서 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="e7b77-116">이 cmdlet은 키 자격 증명 모음의 특정 비밀 또는 모든 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="e7b77-117">예제</span><span class="sxs-lookup"><span data-stu-id="e7b77-117">EXAMPLES</span></span>

### <span data-ttu-id="e7b77-118">예제 1: 키 자격 증명 모음에 있는 모든 비밀의 모든 현재 버전 얻기</span><span class="sxs-lookup"><span data-stu-id="e7b77-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="e7b77-119">이 명령은 Contoso라는 키 자격 증명 모음에 있는 모든 비밀의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7b77-120">예제 2: 특정 비밀의 모든 버전 얻기</span><span class="sxs-lookup"><span data-stu-id="e7b77-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="e7b77-121">이 명령은 Contoso라는 키 자격 증명 모음에서 secret1이라는 비밀의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7b77-122">예제 3: 특정 비밀의 현재 버전 다운로드</span><span class="sxs-lookup"><span data-stu-id="e7b77-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="e7b77-123">이 명령은 Contoso라는 키 자격 증명 모음에서 secret1이라는 비밀의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7b77-124">예제 4: 특정 비밀의 특정 버전 다운로드</span><span class="sxs-lookup"><span data-stu-id="e7b77-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="e7b77-125">이 명령은 Contoso라는 키 자격 증명 모음에서 secret1이라는 비밀의 특정 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7b77-126">예제 5: 특정 비밀의 현재 버전의 일반 텍스트 값 얻기</span><span class="sxs-lookup"><span data-stu-id="e7b77-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'

# Method 1: requires PowerShell >= 7.0
PS C:\> $secretInPlainText = $secret.SecretValue | ConvertFrom-SecureString -AsPlainText

# Method 2: works on older PowerShell versions
PS C:\> $secretValueText = '';
PS C:\> $ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
PS C:\> try {
    $secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}

# Method 3: works in ConstrainedLanguage mode
$secretInPlainText = [pscredential]::new("DoesntMatter", $secret.SecretValue).GetNetworkCredential().Password
```

<span data-ttu-id="e7b77-127">이러한 명령은 ITSecret이라는 비밀의 현재 버전을 다운로드한 다음 해당 비밀의 일반 텍스트 값을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

<span data-ttu-id="e7b77-128">(참고: PowerShell [ConstrainedLanguage](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language)모드에서 작업하는 경우(예: 보안/권한 있는 액세스 Workstations)에서 메서드 3을 사용합니다.)</span><span class="sxs-lookup"><span data-stu-id="e7b77-128">(Note: use method 3 if you are working in PowerShell [ConstrainedLanguage mode](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language), for example, on secure/privileged access workstations.)</span></span>

### <span data-ttu-id="e7b77-129">예제 6: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 모든 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-129">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="e7b77-130">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 모든 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-130">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7b77-131">예제 7: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 비밀 ITSecret을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-131">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="e7b77-132">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 비밀 'secret1'을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-132">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e7b77-133">이 명령은 삭제 날짜와 같은 메타데이터 및 이 삭제된 비밀의 예약된 제거 날짜를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-133">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="e7b77-134">예제 8: 필터링을 사용하여 키 자격 증명 모음에 있는 모든 비밀의 현재 버전 모두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-134">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="e7b77-135">이 명령은 "secret"으로 시작하는 Contoso라는 키 자격 증명 모음에 있는 모든 비밀의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-135">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="e7b77-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7b77-136">PARAMETERS</span></span>

### <span data-ttu-id="e7b77-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b77-137">-DefaultProfile</span></span>
<span data-ttu-id="e7b77-138">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e7b77-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7b77-139">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="e7b77-139">-IncludeVersions</span></span>
<span data-ttu-id="e7b77-140">이 cmdlet이 모든 버전의 비밀을 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-140">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="e7b77-141">현재 버전의 비밀은 목록의 첫 번째 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-141">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="e7b77-142">이 매개 변수를 지정하는 경우 *Name* 및 *VaultName* 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-142">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="e7b77-143">*IncludeVersions* 매개 변수를 지정하지 않으면 이 cmdlet은 지정된 이름의 비밀의 현재 버전을 *얻습니다.*</span><span class="sxs-lookup"><span data-stu-id="e7b77-143">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b77-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7b77-144">-InputObject</span></span>
<span data-ttu-id="e7b77-145">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-145">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b77-146">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e7b77-146">-InRemovedState</span></span>
<span data-ttu-id="e7b77-147">이전에 삭제된 비밀을 출력에 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-147">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b77-148">-Name</span><span class="sxs-lookup"><span data-stu-id="e7b77-148">-Name</span></span>
<span data-ttu-id="e7b77-149">얻을 비밀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-149">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e7b77-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b77-150">-ResourceId</span></span>
<span data-ttu-id="e7b77-151">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-151">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b77-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e7b77-152">-VaultName</span></span>
<span data-ttu-id="e7b77-153">비밀이 속한 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-153">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="e7b77-154">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-154">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b77-155">-Version</span><span class="sxs-lookup"><span data-stu-id="e7b77-155">-Version</span></span>
<span data-ttu-id="e7b77-156">비밀 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-156">Specifies the secret version.</span></span>
<span data-ttu-id="e7b77-157">이 cmdlet은 키 자격 증명 모음 이름, 현재 선택한 환경, 비밀 이름 및 비밀 버전을 기반으로 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b77-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b77-158">CommonParameters</span></span>
<span data-ttu-id="e7b77-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b77-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b77-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7b77-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b77-161">입력</span><span class="sxs-lookup"><span data-stu-id="e7b77-161">INPUTS</span></span>

### <span data-ttu-id="e7b77-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e7b77-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e7b77-163">System.String</span><span class="sxs-lookup"><span data-stu-id="e7b77-163">System.String</span></span>

## <span data-ttu-id="e7b77-164">출력</span><span class="sxs-lookup"><span data-stu-id="e7b77-164">OUTPUTS</span></span>

### <span data-ttu-id="e7b77-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e7b77-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="e7b77-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e7b77-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="e7b77-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e7b77-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="e7b77-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e7b77-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="e7b77-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7b77-169">NOTES</span></span>

## <span data-ttu-id="e7b77-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7b77-170">RELATED LINKS</span></span>

[<span data-ttu-id="e7b77-171">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e7b77-171">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="e7b77-172">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e7b77-172">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="e7b77-173">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e7b77-173">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

