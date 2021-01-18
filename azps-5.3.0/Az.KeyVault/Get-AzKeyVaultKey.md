---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: fa53affab7fe530defcf23f169458ee6813722a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495330"
---
# <span data-ttu-id="30be3-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30be3-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="30be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30be3-102">SYNOPSIS</span></span>
<span data-ttu-id="30be3-103">Key Vault 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="30be3-104">구문</span><span class="sxs-lookup"><span data-stu-id="30be3-104">SYNTAX</span></span>

### <span data-ttu-id="30be3-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="30be3-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="30be3-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="30be3-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="30be3-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="30be3-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="30be3-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="30be3-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="30be3-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="30be3-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="30be3-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="30be3-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="30be3-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30be3-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30be3-123">설명</span><span class="sxs-lookup"><span data-stu-id="30be3-123">DESCRIPTION</span></span>
<span data-ttu-id="30be3-124">**Get-AzKeyVaultKey** cmdlet은 Azure Key Vault 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="30be3-125">이 cmdlet은 **특정 Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** 또는 키 자격 증명 모음 또는 버전별 모든 **KeyBundle** 개체 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="30be3-126">예제</span><span class="sxs-lookup"><span data-stu-id="30be3-126">EXAMPLES</span></span>

### <span data-ttu-id="30be3-127">예제 1: 키 자격 증명 모음의 모든 키 얻기</span><span class="sxs-lookup"><span data-stu-id="30be3-127">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="30be3-128">이 명령은 Contoso라는 키 자격 증명 모음의 모든 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="30be3-129">예제 2: 키의 현재 버전 다운로드</span><span class="sxs-lookup"><span data-stu-id="30be3-129">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="30be3-130">이 명령은 Contoso라는 키 자격 증명 모음에서 test1이라는 키의 현재 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="30be3-131">예제 3: 키의 모든 버전 얻기</span><span class="sxs-lookup"><span data-stu-id="30be3-131">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="30be3-132">이 명령은 Contoso라는 키 자격 증명 모음에서 ITPfx라는 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="30be3-133">예제 4: 특정 버전의 키 다운로드</span><span class="sxs-lookup"><span data-stu-id="30be3-133">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="30be3-134">이 명령은 Contoso라는 키 자격 증명 모음에서 test1이라는 특정 버전의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="30be3-135">이 명령을 실행한 후 $Key 개체를 사용하여 키의 다양한 속성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="30be3-136">예제 5: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 모든 키</span><span class="sxs-lookup"><span data-stu-id="30be3-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="30be3-137">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 모든 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="30be3-138">예제 6: 삭제했지만 이 키 자격 증명 모음에 대해 제거되지 않은 주요 ITPfx를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="30be3-139">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 key test3을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="30be3-140">이 명령은 삭제 날짜와 같은 메타데이터 및 이 삭제된 키의 예약된 제거 날짜를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="30be3-141">예제 7: 필터링을 사용하여 키 자격 증명 모음의 모든 키 얻기</span><span class="sxs-lookup"><span data-stu-id="30be3-141">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="30be3-142">이 명령은 "test"로 시작하는 Contoso라는 키 자격 증명 모음의 모든 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="30be3-143">예제 8: 공개 키를 .pem 파일로 다운로드</span><span class="sxs-lookup"><span data-stu-id="30be3-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="30be3-144">매개 변수를 지정하여 RSA 키의 공개 키를 다운로드할 수 `-OutFile` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="30be3-145">HSM 보호 키를 Azure Key Vault로 가져오는 한 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="30be3-146">참조 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="30be3-146">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="30be3-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30be3-147">PARAMETERS</span></span>

### <span data-ttu-id="30be3-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30be3-148">-DefaultProfile</span></span>
<span data-ttu-id="30be3-149">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="30be3-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30be3-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="30be3-150">-HsmName</span></span>
<span data-ttu-id="30be3-151">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-151">HSM name.</span></span> <span data-ttu-id="30be3-152">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="30be3-153">-HsmObject</span></span>
<span data-ttu-id="30be3-154">HSM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="30be3-155">-HsmResourceId</span></span>
<span data-ttu-id="30be3-156">HSM 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="30be3-157">-IncludeVersions</span></span>
<span data-ttu-id="30be3-158">이 cmdlet이 키의 모든 버전을 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="30be3-159">키의 현재 버전은 목록의 첫 번째 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="30be3-160">이 매개 변수를 지정하는 경우 *Name* 및 *VaultName* 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="30be3-161">*IncludeVersions* 매개 변수를 지정하지 않으면 이 cmdlet은 지정된 이름의 키의 현재 버전을 *얻습니다.*</span><span class="sxs-lookup"><span data-stu-id="30be3-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30be3-162">-InputObject</span></span>
<span data-ttu-id="30be3-163">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-163">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="30be3-164">-InRemovedState</span></span>
<span data-ttu-id="30be3-165">이전에 삭제된 키를 출력에 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-166">-Name</span><span class="sxs-lookup"><span data-stu-id="30be3-166">-Name</span></span>
<span data-ttu-id="30be3-167">얻을 키 번들의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="30be3-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="30be3-168">-OutFile</span></span>
<span data-ttu-id="30be3-169">이 cmdlet에서 키를 저장할 출력 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="30be3-170">공개 키는 기본적으로 PEM 형식으로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-170">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30be3-171">-ResourceId</span></span>
<span data-ttu-id="30be3-172">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="30be3-173">-VaultName</span></span>
<span data-ttu-id="30be3-174">이 cmdlet에서 키를 얻을 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="30be3-175">이 cmdlet은 이 매개 변수가 지정하는 이름 및 선택한 환경에 따라 키 자격 증명 모음의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-176">-Version</span><span class="sxs-lookup"><span data-stu-id="30be3-176">-Version</span></span>
<span data-ttu-id="30be3-177">키 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-177">Specifies the key version.</span></span>
<span data-ttu-id="30be3-178">이 cmdlet은 키 자격 증명 모음 이름, 현재 선택한 환경, 키 이름 및 키 버전을 기반으로 키의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30be3-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30be3-179">CommonParameters</span></span>
<span data-ttu-id="30be3-180">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30be3-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30be3-181">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30be3-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30be3-182">입력</span><span class="sxs-lookup"><span data-stu-id="30be3-182">INPUTS</span></span>

### <span data-ttu-id="30be3-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="30be3-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="30be3-184">System.String</span><span class="sxs-lookup"><span data-stu-id="30be3-184">System.String</span></span>

## <span data-ttu-id="30be3-185">출력</span><span class="sxs-lookup"><span data-stu-id="30be3-185">OUTPUTS</span></span>

### <span data-ttu-id="30be3-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="30be3-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="30be3-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30be3-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="30be3-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="30be3-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="30be3-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30be3-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="30be3-190">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30be3-190">NOTES</span></span>

## <span data-ttu-id="30be3-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30be3-191">RELATED LINKS</span></span>

[<span data-ttu-id="30be3-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30be3-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="30be3-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30be3-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="30be3-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="30be3-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="30be3-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="30be3-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

