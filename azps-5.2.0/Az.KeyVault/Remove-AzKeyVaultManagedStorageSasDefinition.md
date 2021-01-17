---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328124"
---
# <span data-ttu-id="178b8-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="178b8-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="178b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178b8-102">SYNOPSIS</span></span>
<span data-ttu-id="178b8-103">Key Vault 관리 Azure Storage SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="178b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="178b8-104">SYNTAX</span></span>

### <span data-ttu-id="178b8-105">ByDefinitionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="178b8-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="178b8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="178b8-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178b8-107">설명</span><span class="sxs-lookup"><span data-stu-id="178b8-107">DESCRIPTION</span></span>
<span data-ttu-id="178b8-108">Key Vault 관리 Azure Storage SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="178b8-109">또한 이 SAS 정의에 따라 SAS 토큰을 사용하는 데 사용되는 비밀도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="178b8-110">예제</span><span class="sxs-lookup"><span data-stu-id="178b8-110">EXAMPLES</span></span>

### <span data-ttu-id="178b8-111">예제 1: Key Vault 관리 Azure Storage SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="178b8-112">자격 증명 모음 'myvault'에서 'mystorageaccount' 계정과 연결된 Key Vault 관리 저장소 SAS 정의 'mysasdef'를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="178b8-113">예제 2: 사용자 확인 없이 Key Vault 관리 Azure Storage SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="178b8-114">자격 증명 모음 'myvault'에서 'mystorageaccount' 계정과 연결된 Key Vault 관리 저장소 SAS 정의 'mysasdef'를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="178b8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="178b8-115">PARAMETERS</span></span>

### <span data-ttu-id="178b8-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="178b8-116">-AccountName</span></span>
<span data-ttu-id="178b8-117">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-117">Storage account name.</span></span>
<span data-ttu-id="178b8-118">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="178b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178b8-119">-DefaultProfile</span></span>
<span data-ttu-id="178b8-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="178b8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="178b8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="178b8-121">-Force</span></span>
<span data-ttu-id="178b8-122">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="178b8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="178b8-123">-InputObject</span></span>
<span data-ttu-id="178b8-124">ManagedStorageSasDefinition 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="178b8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="178b8-125">-Name</span></span>
<span data-ttu-id="178b8-126">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-126">Storage sas definition name.</span></span>
<span data-ttu-id="178b8-127">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="178b8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="178b8-128">-PassThru</span></span>
<span data-ttu-id="178b8-129">Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="178b8-130">이 스위치를 지정하면 cmdlet은 삭제된 관리되는 저장소 계정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="178b8-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="178b8-131">-VaultName</span></span>
<span data-ttu-id="178b8-132">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-132">Vault name.</span></span>
<span data-ttu-id="178b8-133">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="178b8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="178b8-134">-Confirm</span></span>
<span data-ttu-id="178b8-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="178b8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178b8-136">-WhatIf</span></span>
<span data-ttu-id="178b8-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="178b8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178b8-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="178b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178b8-139">CommonParameters</span></span>
<span data-ttu-id="178b8-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178b8-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="178b8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178b8-142">입력</span><span class="sxs-lookup"><span data-stu-id="178b8-142">INPUTS</span></span>

### <span data-ttu-id="178b8-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="178b8-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="178b8-144">출력</span><span class="sxs-lookup"><span data-stu-id="178b8-144">OUTPUTS</span></span>

### <span data-ttu-id="178b8-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="178b8-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="178b8-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="178b8-146">NOTES</span></span>

## <span data-ttu-id="178b8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="178b8-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

