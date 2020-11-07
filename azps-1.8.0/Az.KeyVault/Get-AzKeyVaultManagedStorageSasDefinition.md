---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff384b456d6cbaac3fa0c28f01038a60b211dfca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867969"
---
# <span data-ttu-id="ab6fd-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ab6fd-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="ab6fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6fd-103">키 보관소 관리 저장소 SAS 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="ab6fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab6fd-104">SYNTAX</span></span>

### <span data-ttu-id="ab6fd-105">ByDefinitionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab6fd-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab6fd-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab6fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab6fd-107">DESCRIPTION</span></span>
<span data-ttu-id="ab6fd-108">정의 이름이 지정 된 경우 키 보관소 관리 저장소 SAS 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="ab6fd-109">정의 이름을 지정 하지 않으면 자격 증명 모음에 지정 된 키 보관소 관리 저장소 계정과 연결 된 모든 SAS 정의가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="ab6fd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ab6fd-110">EXAMPLES</span></span>

### <span data-ttu-id="ab6fd-111">예제 1: 모든 키 자격 증명 모음 관리 저장소 SAS 정의 나열</span><span class="sxs-lookup"><span data-stu-id="ab6fd-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="ab6fd-112">키 자격 증명 모음 ' mystorageaccount '와 연결 된 모든 SAS 정의가 자격 증명 모음 ' myvault '에 의해 관리 됨</span><span class="sxs-lookup"><span data-stu-id="ab6fd-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="ab6fd-113">예제 2: 키 보관소 관리 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="ab6fd-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="ab6fd-114">' Myvault ' 자격 증명 모음에서 관리 하는 키 보관소 관리 저장소 계정 ' mystorageaccount '와 연결 된 SAS 정의 ' accountsas '의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="ab6fd-115">예제 3: 필터링을 사용 하 여 모든 키 자격 증명 모음 관리 저장소 SAS 정의 나열</span><span class="sxs-lookup"><span data-stu-id="ab6fd-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="ab6fd-116">키 자격 증명 모음 관리 저장소 계정 ' mystorageaccount '이 "Account"로 시작 하는 자격 증명 모음 ' myvault '에 의해 관리 되는 모든 SAS 정의를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="ab6fd-117">변수</span><span class="sxs-lookup"><span data-stu-id="ab6fd-117">PARAMETERS</span></span>

### <span data-ttu-id="ab6fd-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ab6fd-118">-AccountName</span></span>
<span data-ttu-id="ab6fd-119">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="ab6fd-119">Vault name.</span></span>
<span data-ttu-id="ab6fd-120">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ab6fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6fd-121">-DefaultProfile</span></span>
<span data-ttu-id="ab6fd-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ab6fd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab6fd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab6fd-123">-InputObject</span></span>
<span data-ttu-id="ab6fd-124">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="ab6fd-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ab6fd-125">-InRemovedState</span></span>
<span data-ttu-id="ab6fd-126">출력에 이전에 삭제 된 저장소 sas 정의를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="ab6fd-127">-이름</span><span class="sxs-lookup"><span data-stu-id="ab6fd-127">-Name</span></span>
<span data-ttu-id="ab6fd-128">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-128">Storage sas definition name.</span></span>
<span data-ttu-id="ab6fd-129">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="ab6fd-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ab6fd-130">-VaultName</span></span>
<span data-ttu-id="ab6fd-131">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="ab6fd-131">Vault name.</span></span>
<span data-ttu-id="ab6fd-132">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ab6fd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6fd-133">CommonParameters</span></span>
<span data-ttu-id="ab6fd-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6fd-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab6fd-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6fd-136">입력</span><span class="sxs-lookup"><span data-stu-id="ab6fd-136">INPUTS</span></span>

### <span data-ttu-id="ab6fd-137">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ab6fd-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ab6fd-138">출력</span><span class="sxs-lookup"><span data-stu-id="ab6fd-138">OUTPUTS</span></span>

### <span data-ttu-id="ab6fd-139">Microsoft. KeyVault. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ab6fd-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="ab6fd-140">Microsoft. KeyVault. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ab6fd-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="ab6fd-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ab6fd-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="ab6fd-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ab6fd-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="ab6fd-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ab6fd-143">NOTES</span></span>

## <span data-ttu-id="ab6fd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab6fd-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

