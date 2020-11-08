---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: af2baec6b25b770c30f5f3207e6ed6b6a4b423f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056704"
---
# <span data-ttu-id="75521-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="75521-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="75521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75521-102">SYNOPSIS</span></span>
<span data-ttu-id="75521-103">키 보관소의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="75521-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75521-104">SYNTAX</span></span>

### <span data-ttu-id="75521-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="75521-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="75521-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="75521-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="75521-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="75521-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="75521-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="75521-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="75521-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75521-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="75521-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75521-114">설명은</span><span class="sxs-lookup"><span data-stu-id="75521-114">DESCRIPTION</span></span>
<span data-ttu-id="75521-115">**AzKeyVaultSecret** cmdlet은 키 보관소의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="75521-116">이 cmdlet은 키 자격 증명 모음의 특정 비밀 또는 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="75521-117">예제의</span><span class="sxs-lookup"><span data-stu-id="75521-117">EXAMPLES</span></span>

### <span data-ttu-id="75521-118">예제 1: 키 보관소에 있는 모든 비밀에 대 한 모든 최신 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="75521-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="75521-119">이 명령은 Contoso 라는 키 보관소에 있는 모든 비밀의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="75521-120">예제 2: 특정 비밀의 모든 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="75521-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="75521-121">이 명령은 Contoso 라는 키 보관소에 secret1 이라는 모든 버전의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="75521-122">예제 3: 특정 비밀 정보의 현재 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="75521-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="75521-123">이 명령은 Contoso 라는 키 보관소에 있는 secret1 이라는 비밀의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="75521-124">예제 4: 특정 보안 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="75521-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="75521-125">이 명령은 Contoso 라는 키 보관소에 있는 secret1 이라는 특정 버전의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="75521-126">예제 5: 특정 비밀의 현재 버전에 대 한 일반 텍스트 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="75521-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="75521-127">이러한 명령은 ITSecret 라는 최신 버전의 비밀을 얻은 다음 해당 비밀의 일반 텍스트 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="75521-128">예제 6: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="75521-129">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="75521-130">예제 7: 삭제 되었지만이 키 보관소에는 제거 되지 않은 비밀 ITSecret를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="75521-131">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 비밀 ' secret1 '을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="75521-132">이 명령은 삭제 날짜와 같은 메타 데이터를 반환 하 고, 해당 비밀의 예정 된 제거 날짜</span><span class="sxs-lookup"><span data-stu-id="75521-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="75521-133">예제 8: 필터링을 사용 하 여 키 보관소에 있는 모든 최신 버전의 비밀 가져오기</span><span class="sxs-lookup"><span data-stu-id="75521-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="75521-134">이 명령은 "비밀"으로 시작 하는 Contoso 라는 키 보관소에 있는 모든 비밀의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="75521-135">변수</span><span class="sxs-lookup"><span data-stu-id="75521-135">PARAMETERS</span></span>

### <span data-ttu-id="75521-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75521-136">-DefaultProfile</span></span>
<span data-ttu-id="75521-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="75521-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75521-138">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="75521-138">-IncludeVersions</span></span>
<span data-ttu-id="75521-139">이 cmdlet이 모든 보안 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-139">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="75521-140">현재 버전의 비밀은 목록의 첫 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="75521-140">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="75521-141">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-141">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="75521-142">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75521-142">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="75521-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75521-143">-InputObject</span></span>
<span data-ttu-id="75521-144">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="75521-144">KeyVault Object.</span></span>

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

### <span data-ttu-id="75521-145">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="75521-145">-InRemovedState</span></span>
<span data-ttu-id="75521-146">이전에 삭제 한 비밀을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-146">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="75521-147">-이름</span><span class="sxs-lookup"><span data-stu-id="75521-147">-Name</span></span>
<span data-ttu-id="75521-148">가져올 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-148">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75521-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75521-149">-ResourceId</span></span>
<span data-ttu-id="75521-150">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="75521-150">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="75521-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75521-151">-VaultName</span></span>
<span data-ttu-id="75521-152">비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-152">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="75521-153">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-153">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="75521-154">-버전</span><span class="sxs-lookup"><span data-stu-id="75521-154">-Version</span></span>
<span data-ttu-id="75521-155">비밀 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-155">Specifies the secret version.</span></span>
<span data-ttu-id="75521-156">이 cmdlet은 키 보관소 이름, 현재 선택 된 환경, 비밀 이름 및 비밀 버전을 기준으로 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-156">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="75521-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75521-157">CommonParameters</span></span>
<span data-ttu-id="75521-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75521-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75521-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75521-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75521-160">입력</span><span class="sxs-lookup"><span data-stu-id="75521-160">INPUTS</span></span>

### <span data-ttu-id="75521-161">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="75521-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="75521-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75521-162">System.String</span></span>

## <span data-ttu-id="75521-163">출력</span><span class="sxs-lookup"><span data-stu-id="75521-163">OUTPUTS</span></span>

### <span data-ttu-id="75521-164">Microsoft. KeyVault. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="75521-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="75521-165">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="75521-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="75521-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="75521-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="75521-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="75521-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="75521-168">상속자</span><span class="sxs-lookup"><span data-stu-id="75521-168">NOTES</span></span>

## <span data-ttu-id="75521-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75521-169">RELATED LINKS</span></span>

[<span data-ttu-id="75521-170">제거-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="75521-170">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="75521-171">실행 취소-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="75521-171">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="75521-172">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="75521-172">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

