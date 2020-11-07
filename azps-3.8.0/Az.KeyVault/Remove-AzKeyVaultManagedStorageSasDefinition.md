---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878485"
---
# <span data-ttu-id="27b89-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="27b89-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="27b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b89-102">SYNOPSIS</span></span>
<span data-ttu-id="27b89-103">키 보관소 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="27b89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27b89-104">SYNTAX</span></span>

### <span data-ttu-id="27b89-105">ByDefinitionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="27b89-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27b89-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27b89-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b89-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27b89-107">DESCRIPTION</span></span>
<span data-ttu-id="27b89-108">키 보관소 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="27b89-109">이는이 SAS 정의에 따라 SAS 토큰을 가져오는 데 사용 되는 비밀도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="27b89-110">예제의</span><span class="sxs-lookup"><span data-stu-id="27b89-110">EXAMPLES</span></span>

### <span data-ttu-id="27b89-111">예제 1: 키 보관소 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="27b89-112">자격 증명 모음 ' mystorageaccount '와 연결 된 키 보관소 관리 저장소 SAS 정의 ' mysasdef '를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="27b89-113">예제 2: 사용자 확인 없이 키 자격 증명 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="27b89-114">자격 증명 모음 ' mystorageaccount '와 연결 된 키 보관소 관리 저장소 SAS 정의 ' mysasdef '를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="27b89-115">변수</span><span class="sxs-lookup"><span data-stu-id="27b89-115">PARAMETERS</span></span>

### <span data-ttu-id="27b89-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="27b89-116">-AccountName</span></span>
<span data-ttu-id="27b89-117">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-117">Storage account name.</span></span>
<span data-ttu-id="27b89-118">Cmdlet은 관리 되는 저장소 계정 이름의 FQDN을 자격 증명 모음 이름, 현재 선택한 환경 및 저장소 계정 이름과 동일 하 게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="27b89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b89-119">-DefaultProfile</span></span>
<span data-ttu-id="27b89-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="27b89-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27b89-121">-Force</span><span class="sxs-lookup"><span data-stu-id="27b89-121">-Force</span></span>
<span data-ttu-id="27b89-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="27b89-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27b89-123">-InputObject</span></span>
<span data-ttu-id="27b89-124">ManagedStorageSasDefinition 개체.</span><span class="sxs-lookup"><span data-stu-id="27b89-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-125">-이름</span><span class="sxs-lookup"><span data-stu-id="27b89-125">-Name</span></span>
<span data-ttu-id="27b89-126">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-126">Storage sas definition name.</span></span>
<span data-ttu-id="27b89-127">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27b89-128">-PassThru</span></span>
<span data-ttu-id="27b89-129">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="27b89-130">이 스위치가 지정 된 경우 cmdlet은 삭제 된 관리 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="27b89-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="27b89-131">-VaultName</span></span>
<span data-ttu-id="27b89-132">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="27b89-132">Vault name.</span></span>
<span data-ttu-id="27b89-133">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="27b89-134">-확인</span><span class="sxs-lookup"><span data-stu-id="27b89-134">-Confirm</span></span>
<span data-ttu-id="27b89-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b89-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b89-136">-WhatIf</span></span>
<span data-ttu-id="27b89-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b89-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b89-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b89-139">CommonParameters</span></span>
<span data-ttu-id="27b89-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b89-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b89-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27b89-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b89-142">입력</span><span class="sxs-lookup"><span data-stu-id="27b89-142">INPUTS</span></span>

### <span data-ttu-id="27b89-143">Microsoft. KeyVault. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="27b89-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="27b89-144">출력</span><span class="sxs-lookup"><span data-stu-id="27b89-144">OUTPUTS</span></span>

### <span data-ttu-id="27b89-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="27b89-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="27b89-146">상속자</span><span class="sxs-lookup"><span data-stu-id="27b89-146">NOTES</span></span>

## <span data-ttu-id="27b89-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27b89-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

