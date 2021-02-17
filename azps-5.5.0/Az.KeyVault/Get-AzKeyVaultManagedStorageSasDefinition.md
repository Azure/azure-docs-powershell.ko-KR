---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188172"
---
# <span data-ttu-id="e35b7-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e35b7-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e35b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e35b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e35b7-103">Key Vault 관리 저장소 SAS 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="e35b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e35b7-104">SYNTAX</span></span>

### <span data-ttu-id="e35b7-105">ByDefinitionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e35b7-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e35b7-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e35b7-107">설명</span><span class="sxs-lookup"><span data-stu-id="e35b7-107">DESCRIPTION</span></span>
<span data-ttu-id="e35b7-108">정의 이름이 지정된 경우 Key Vault 관리 저장소 SAS 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="e35b7-109">정의 이름을 지정하지 않으면 자격 증명 모음에 지정된 Key Vault 관리되는 Storage 계정과 연결된 모든 SAS 정의가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="e35b7-110">예제</span><span class="sxs-lookup"><span data-stu-id="e35b7-110">EXAMPLES</span></span>

### <span data-ttu-id="e35b7-111">예제 1: 모든 Key Vault 관리 저장소 SAS 정의 나열</span><span class="sxs-lookup"><span data-stu-id="e35b7-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="e35b7-112">자격 증명 모음 'myvault'에서 관리되는 Key Vault 관리 스토리지 계정 'mystorageaccount'와 연결된 모든 SAS 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="e35b7-113">예제 2: Key Vault 관리 저장소 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="e35b7-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="e35b7-114">자격 증명 모음 'myvault'에서 관리하는 Key Vault 관리 스토리지 계정 'mystorageaccount'와 연결된 SAS 정의 'accountsas'의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="e35b7-115">예제 3: 필터링을 사용하여 모든 Key Vault 관리 저장소 SAS 정의 나열</span><span class="sxs-lookup"><span data-stu-id="e35b7-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="e35b7-116">"account"로 시작하는 자격 증명 모음 'myvault'에서 관리하는 Key Vault 관리 스토리지 계정 'mystorageaccount'와 연결된 모든 SAS 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="e35b7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e35b7-117">PARAMETERS</span></span>

### <span data-ttu-id="e35b7-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e35b7-118">-AccountName</span></span>
<span data-ttu-id="e35b7-119">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-119">Vault name.</span></span>
<span data-ttu-id="e35b7-120">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35b7-121">-DefaultProfile</span></span>
<span data-ttu-id="e35b7-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e35b7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e35b7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e35b7-123">-InputObject</span></span>
<span data-ttu-id="e35b7-124">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-124">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e35b7-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e35b7-125">-InRemovedState</span></span>
<span data-ttu-id="e35b7-126">이전에 삭제된 저장소 sas 정의를 출력에 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="e35b7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e35b7-127">-Name</span></span>
<span data-ttu-id="e35b7-128">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-128">Storage sas definition name.</span></span>
<span data-ttu-id="e35b7-129">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35b7-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e35b7-130">-VaultName</span></span>
<span data-ttu-id="e35b7-131">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-131">Vault name.</span></span>
<span data-ttu-id="e35b7-132">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35b7-133">CommonParameters</span></span>
<span data-ttu-id="e35b7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e35b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35b7-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e35b7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35b7-136">입력</span><span class="sxs-lookup"><span data-stu-id="e35b7-136">INPUTS</span></span>

### <span data-ttu-id="e35b7-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e35b7-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e35b7-138">출력</span><span class="sxs-lookup"><span data-stu-id="e35b7-138">OUTPUTS</span></span>

### <span data-ttu-id="e35b7-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e35b7-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="e35b7-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e35b7-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="e35b7-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e35b7-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="e35b7-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e35b7-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="e35b7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e35b7-143">NOTES</span></span>

## <span data-ttu-id="e35b7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e35b7-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

