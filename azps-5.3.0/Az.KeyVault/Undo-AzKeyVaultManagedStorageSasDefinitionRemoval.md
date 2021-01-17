---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491946"
---
# <span data-ttu-id="52a81-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="52a81-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="52a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a81-102">SYNOPSIS</span></span>
<span data-ttu-id="52a81-103">이전에 삭제된 KeyVault 관리 저장소 SAS 정의를 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="52a81-104">구문</span><span class="sxs-lookup"><span data-stu-id="52a81-104">SYNTAX</span></span>

### <span data-ttu-id="52a81-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="52a81-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a81-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="52a81-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a81-107">설명</span><span class="sxs-lookup"><span data-stu-id="52a81-107">DESCRIPTION</span></span>
<span data-ttu-id="52a81-108">**Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** 명령은 이 자격 증명 모음에 대해 소프트 삭제를 사용하도록 설정하고 복구 간격 동안 복구 시도가 발생하면 이전에 삭제된 관리 저장소 SAS 정의를 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="52a81-109">예제</span><span class="sxs-lookup"><span data-stu-id="52a81-109">EXAMPLES</span></span>

### <span data-ttu-id="52a81-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="52a81-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="52a81-111">이 명령 시퀀스는 지정된 저장소 SAS 정의가 삭제된 상태의 자격 증명 모음에 있는지 여부를 판단합니다. 후속 명령은 삭제된 sas 정의를 복구하여 다시 활성 상태로 되돌려 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="52a81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52a81-112">PARAMETERS</span></span>

### <span data-ttu-id="52a81-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52a81-113">-AccountName</span></span>
<span data-ttu-id="52a81-114">KeyVault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="52a81-115">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 SAS 정의의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a81-116">-DefaultProfile</span></span>
<span data-ttu-id="52a81-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a81-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a81-118">-InputObject</span></span>
<span data-ttu-id="52a81-119">삭제된 관리 저장소 SAS 정의 개체</span><span class="sxs-lookup"><span data-stu-id="52a81-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a81-120">-Name</span><span class="sxs-lookup"><span data-stu-id="52a81-120">-Name</span></span>
<span data-ttu-id="52a81-121">KeyVault 관리 저장소 SAS 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="52a81-122">Cmdlet은 자격 증명 모음 이름, 현재 선택된 환경, 관리되는 저장소 계정의 이름 및 SAS 정의의 이름에서 대상의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a81-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52a81-123">-VaultName</span></span>
<span data-ttu-id="52a81-124">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-124">Vault name.</span></span>
<span data-ttu-id="52a81-125">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a81-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52a81-126">-Confirm</span></span>
<span data-ttu-id="52a81-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a81-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a81-128">-WhatIf</span></span>
<span data-ttu-id="52a81-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="52a81-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a81-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a81-131">CommonParameters</span></span>
<span data-ttu-id="52a81-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52a81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a81-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52a81-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a81-134">입력</span><span class="sxs-lookup"><span data-stu-id="52a81-134">INPUTS</span></span>

### <span data-ttu-id="52a81-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="52a81-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="52a81-136">출력</span><span class="sxs-lookup"><span data-stu-id="52a81-136">OUTPUTS</span></span>

### <span data-ttu-id="52a81-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="52a81-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="52a81-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52a81-138">NOTES</span></span>

## <span data-ttu-id="52a81-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52a81-139">RELATED LINKS</span></span>
