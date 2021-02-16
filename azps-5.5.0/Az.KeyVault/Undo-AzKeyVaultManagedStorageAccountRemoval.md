---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 3d854d6b820f6c2e23d99e3397173ec45d5b7697
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185449"
---
# <span data-ttu-id="763d1-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="763d1-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="763d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="763d1-102">SYNOPSIS</span></span>
<span data-ttu-id="763d1-103">이전에 삭제된 KeyVault 관리 저장소 계정을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="763d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="763d1-104">SYNTAX</span></span>

### <span data-ttu-id="763d1-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="763d1-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="763d1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="763d1-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="763d1-107">설명</span><span class="sxs-lookup"><span data-stu-id="763d1-107">DESCRIPTION</span></span>
<span data-ttu-id="763d1-108">이 자격 증명 모음에 대해 소프트 삭제를 사용하도록 설정하고 복구 간격 동안 복구 시도가 발생하면 **Undo-AzKeyVaultManagedStorageAccountRemoval** 명령은 이전에 삭제된 관리되는 저장소 계정을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="763d1-109">예제</span><span class="sxs-lookup"><span data-stu-id="763d1-109">EXAMPLES</span></span>

### <span data-ttu-id="763d1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="763d1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="763d1-111">이 명령 시퀀스는 지정된 저장소 계정이 삭제된 상태의 자격 증명 모음에 있는지 여부를 판단합니다. 후속 명령은 삭제된 저장소 계정을 복구하여 다시 활성 상태로 되돌려 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="763d1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="763d1-112">PARAMETERS</span></span>

### <span data-ttu-id="763d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763d1-113">-DefaultProfile</span></span>
<span data-ttu-id="763d1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="763d1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="763d1-115">-InputObject</span></span>
<span data-ttu-id="763d1-116">삭제된 Managed Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="763d1-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="763d1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="763d1-117">-Name</span></span>
<span data-ttu-id="763d1-118">KeyVault 관리 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="763d1-119">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정의 이름에서 대상의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="763d1-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="763d1-120">-VaultName</span></span>
<span data-ttu-id="763d1-121">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-121">Vault name.</span></span>
<span data-ttu-id="763d1-122">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="763d1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="763d1-123">-Confirm</span></span>
<span data-ttu-id="763d1-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="763d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="763d1-125">-WhatIf</span></span>
<span data-ttu-id="763d1-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="763d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="763d1-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="763d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763d1-128">CommonParameters</span></span>
<span data-ttu-id="763d1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="763d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763d1-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="763d1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763d1-131">입력</span><span class="sxs-lookup"><span data-stu-id="763d1-131">INPUTS</span></span>

### <span data-ttu-id="763d1-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="763d1-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="763d1-133">출력</span><span class="sxs-lookup"><span data-stu-id="763d1-133">OUTPUTS</span></span>

### <span data-ttu-id="763d1-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763d1-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="763d1-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="763d1-135">NOTES</span></span>

## <span data-ttu-id="763d1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="763d1-136">RELATED LINKS</span></span>
