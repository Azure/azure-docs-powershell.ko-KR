---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: aa8306070eb560deb465cbaa9ddae2bce24c5600
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534323"
---
# <span data-ttu-id="ae8f5-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae8f5-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="ae8f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8f5-103">키 보관소의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae8f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae8f5-104">SYNTAX</span></span>

### <span data-ttu-id="ae8f5-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae8f5-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="ae8f5-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="ae8f5-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="ae8f5-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="ae8f5-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="ae8f5-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="ae8f5-111">ByResourceIdVaultName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="ae8f5-112">ByResourceIdSecretName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae8f5-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="ae8f5-113">ByResourceIdSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae8f5-114">설명은</span><span class="sxs-lookup"><span data-stu-id="ae8f5-114">DESCRIPTION</span></span>
<span data-ttu-id="ae8f5-115">**AzureKeyVaultSecret** cmdlet은 키 보관소의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-115">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="ae8f5-116">이 cmdlet은 키 자격 증명 모음의 특정 비밀 또는 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="ae8f5-117">예제의</span><span class="sxs-lookup"><span data-stu-id="ae8f5-117">EXAMPLES</span></span>

### <span data-ttu-id="ae8f5-118">예제 1: 키 보관소에 있는 모든 비밀에 대 한 모든 최신 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae8f5-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso'

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

<span data-ttu-id="ae8f5-119">이 명령은 Contoso 라는 키 보관소에 있는 모든 비밀의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae8f5-120">예제 2: 특정 비밀의 모든 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae8f5-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

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

<span data-ttu-id="ae8f5-121">이 명령은 Contoso 라는 키 보관소에 secret1 이라는 모든 버전의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae8f5-122">예제 3: 특정 비밀 정보의 현재 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae8f5-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

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

<span data-ttu-id="ae8f5-123">이 명령은 Contoso 라는 키 보관소에 있는 secret1 이라는 비밀의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae8f5-124">예제 4: 특정 보안 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae8f5-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

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

<span data-ttu-id="ae8f5-125">이 명령은 Contoso 라는 키 보관소에 있는 secret1 이라는 특정 버전의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae8f5-126">예제 5: 특정 비밀의 현재 버전에 대 한 일반 텍스트 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="ae8f5-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="ae8f5-127">이러한 명령은 ITSecret 라는 최신 버전의 비밀을 얻은 다음 해당 비밀의 일반 텍스트 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="ae8f5-128">예제 6: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState

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

<span data-ttu-id="ae8f5-129">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="ae8f5-130">예제 7: 삭제 되었지만이 키 보관소에는 제거 되지 않은 비밀 ITSecret를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'secret1' -InRemovedState

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

<span data-ttu-id="ae8f5-131">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 비밀 ' secret1 '을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="ae8f5-132">이 명령은 삭제 날짜와 같은 메타 데이터를 반환 하 고, 해당 비밀의 예정 된 제거 날짜</span><span class="sxs-lookup"><span data-stu-id="ae8f5-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="ae8f5-133">변수</span><span class="sxs-lookup"><span data-stu-id="ae8f5-133">PARAMETERS</span></span>

### <span data-ttu-id="ae8f5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8f5-134">-DefaultProfile</span></span>
<span data-ttu-id="ae8f5-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae8f5-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8f5-136">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="ae8f5-136">-IncludeVersions</span></span>
<span data-ttu-id="ae8f5-137">이 cmdlet이 모든 보안 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-137">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="ae8f5-138">현재 버전의 비밀은 목록의 첫 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-138">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="ae8f5-139">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-139">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="ae8f5-140">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-140">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="ae8f5-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae8f5-141">-InputObject</span></span>
<span data-ttu-id="ae8f5-142">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-142">KeyVault Object.</span></span>

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

### <span data-ttu-id="ae8f5-143">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ae8f5-143">-InRemovedState</span></span>
<span data-ttu-id="ae8f5-144">이전에 삭제 한 비밀을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-144">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="ae8f5-145">-이름</span><span class="sxs-lookup"><span data-stu-id="ae8f5-145">-Name</span></span>
<span data-ttu-id="ae8f5-146">가져올 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-146">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="ae8f5-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae8f5-147">-ResourceId</span></span>
<span data-ttu-id="ae8f5-148">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-148">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="ae8f5-149">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae8f5-149">-VaultName</span></span>
<span data-ttu-id="ae8f5-150">비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-150">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="ae8f5-151">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-151">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="ae8f5-152">-버전</span><span class="sxs-lookup"><span data-stu-id="ae8f5-152">-Version</span></span>
<span data-ttu-id="ae8f5-153">비밀 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-153">Specifies the secret version.</span></span>
<span data-ttu-id="ae8f5-154">이 cmdlet은 키 보관소 이름, 현재 선택 된 환경, 비밀 이름 및 비밀 버전을 기준으로 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-154">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="ae8f5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8f5-155">CommonParameters</span></span>
<span data-ttu-id="ae8f5-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8f5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8f5-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae8f5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8f5-158">입력</span><span class="sxs-lookup"><span data-stu-id="ae8f5-158">INPUTS</span></span>

### <span data-ttu-id="ae8f5-159">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ae8f5-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ae8f5-160">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae8f5-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ae8f5-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae8f5-161">System.String</span></span>

## <span data-ttu-id="ae8f5-162">출력</span><span class="sxs-lookup"><span data-stu-id="ae8f5-162">OUTPUTS</span></span>

### <span data-ttu-id="ae8f5-163">Microsoft. KeyVault. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ae8f5-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="ae8f5-164">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae8f5-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="ae8f5-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ae8f5-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="ae8f5-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae8f5-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="ae8f5-167">상속자</span><span class="sxs-lookup"><span data-stu-id="ae8f5-167">NOTES</span></span>

## <span data-ttu-id="ae8f5-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae8f5-168">RELATED LINKS</span></span>

[<span data-ttu-id="ae8f5-169">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae8f5-169">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="ae8f5-170">실행 취소-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="ae8f5-170">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="ae8f5-171">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae8f5-171">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

