---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219042"
---
# <span data-ttu-id="c1815-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="c1815-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="c1815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1815-102">SYNOPSIS</span></span>
<span data-ttu-id="c1815-103">이전에 삭제 된 KeyVault 관리 저장소 SAS 정의를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="c1815-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1815-104">SYNTAX</span></span>

### <span data-ttu-id="c1815-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c1815-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1815-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1815-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1815-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c1815-107">DESCRIPTION</span></span>
<span data-ttu-id="c1815-108">**AzKeyVaultManagedStorageSasDefinitionRemoval** 명령은이 자격 증명 모음에 대 한 소프트 삭제를 사용 하도록 설정 하 고 복구 간격 동안 복구 시도가 발생 하는 경우 이전에 삭제 된 관리 되는 저장소 SAS 정의를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="c1815-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c1815-109">EXAMPLES</span></span>

### <span data-ttu-id="c1815-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1815-110">Example 1</span></span>
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

<span data-ttu-id="c1815-111">이 명령 순서에 따라 지정 된 저장소 SA 정의가 자격 증명 모음에 삭제 된 상태로 있는지 여부를 결정 합니다. 후속 명령은 삭제 된 sas 정의를 복구 하 고 활성 상태로 다시 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="c1815-112">변수</span><span class="sxs-lookup"><span data-stu-id="c1815-112">PARAMETERS</span></span>

### <span data-ttu-id="c1815-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1815-113">-AccountName</span></span>
<span data-ttu-id="c1815-114">KeyVault-관리 되는 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="c1815-115">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 관리 되는 저장소 계정 이름에서 관리 되는 저장소 SAS 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="c1815-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1815-116">-DefaultProfile</span></span>
<span data-ttu-id="c1815-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1815-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1815-118">-InputObject</span></span>
<span data-ttu-id="c1815-119">관리 되는 저장소 SAS 정의 개체 삭제 됨</span><span class="sxs-lookup"><span data-stu-id="c1815-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="c1815-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c1815-120">-Name</span></span>
<span data-ttu-id="c1815-121">KeyVault 관리 저장소 SAS 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="c1815-122">Cmdlet은 자격 증명 이름, 현재 선택 된 환경, 관리 되는 저장소 계정의 이름 및 SAS 정의 이름에 대 한 대상의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="c1815-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c1815-123">-VaultName</span></span>
<span data-ttu-id="c1815-124">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="c1815-124">Vault name.</span></span>
<span data-ttu-id="c1815-125">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c1815-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c1815-126">-Confirm</span></span>
<span data-ttu-id="c1815-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1815-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1815-128">-WhatIf</span></span>
<span data-ttu-id="c1815-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1815-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1815-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1815-131">CommonParameters</span></span>
<span data-ttu-id="c1815-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1815-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1815-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1815-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1815-134">입력</span><span class="sxs-lookup"><span data-stu-id="c1815-134">INPUTS</span></span>

### <span data-ttu-id="c1815-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c1815-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="c1815-136">출력</span><span class="sxs-lookup"><span data-stu-id="c1815-136">OUTPUTS</span></span>

### <span data-ttu-id="c1815-137">Microsoft. KeyVault. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="c1815-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="c1815-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c1815-138">NOTES</span></span>

## <span data-ttu-id="c1815-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1815-139">RELATED LINKS</span></span>
