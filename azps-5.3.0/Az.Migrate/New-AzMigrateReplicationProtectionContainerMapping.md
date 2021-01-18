---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492793"
---
# <span data-ttu-id="68ad4-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="68ad4-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="68ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="68ad4-103">보호 컨테이너 매핑을 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="68ad4-104">구문</span><span class="sxs-lookup"><span data-stu-id="68ad4-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="68ad4-105">설명</span><span class="sxs-lookup"><span data-stu-id="68ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="68ad4-106">보호 컨테이너 매핑을 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="68ad4-107">예제</span><span class="sxs-lookup"><span data-stu-id="68ad4-107">EXAMPLES</span></span>

### <span data-ttu-id="68ad4-108">예제 1: 매핑 만들기</span><span class="sxs-lookup"><span data-stu-id="68ad4-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="68ad4-109">매핑 만들기</span><span class="sxs-lookup"><span data-stu-id="68ad4-109">Create a mapping</span></span>

## <span data-ttu-id="68ad4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68ad4-110">PARAMETERS</span></span>

### <span data-ttu-id="68ad4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68ad4-111">-AsJob</span></span>
<span data-ttu-id="68ad4-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="68ad4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="68ad4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ad4-113">-DefaultProfile</span></span>
<span data-ttu-id="68ad4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="68ad4-115">-FabricName</span></span>
<span data-ttu-id="68ad4-116">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-116">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="68ad4-117">-MappingName</span></span>
<span data-ttu-id="68ad4-118">보호 컨테이너 매핑 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-118">Protection container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68ad4-119">-NoWait</span></span>
<span data-ttu-id="68ad4-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="68ad4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68ad4-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="68ad4-121">-PolicyId</span></span>
<span data-ttu-id="68ad4-122">적용 가능한 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-122">Applicable policy.</span></span>

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

### <span data-ttu-id="68ad4-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="68ad4-123">-ProtectionContainerName</span></span>
<span data-ttu-id="68ad4-124">보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-124">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="68ad4-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="68ad4-126">페어링에 대한 공급자 특정 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="68ad4-127">생성을 위해 PROVIDERSPECIFICINPUT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="68ad4-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ad4-128">-ResourceGroupName</span></span>
<span data-ttu-id="68ad4-129">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-129">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="68ad4-130">-ResourceName</span></span>
<span data-ttu-id="68ad4-131">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-131">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68ad4-132">-SubscriptionId</span></span>
<span data-ttu-id="68ad4-133">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-133">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ad4-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="68ad4-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="68ad4-135">대상 고유 보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="68ad4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68ad4-136">-Confirm</span></span>
<span data-ttu-id="68ad4-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ad4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ad4-138">-WhatIf</span></span>
<span data-ttu-id="68ad4-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="68ad4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ad4-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ad4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ad4-141">CommonParameters</span></span>
<span data-ttu-id="68ad4-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ad4-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68ad4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ad4-144">입력</span><span class="sxs-lookup"><span data-stu-id="68ad4-144">INPUTS</span></span>

## <span data-ttu-id="68ad4-145">출력</span><span class="sxs-lookup"><span data-stu-id="68ad4-145">OUTPUTS</span></span>

### <span data-ttu-id="68ad4-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="68ad4-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="68ad4-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68ad4-147">NOTES</span></span>

<span data-ttu-id="68ad4-148">별칭</span><span class="sxs-lookup"><span data-stu-id="68ad4-148">ALIASES</span></span>

<span data-ttu-id="68ad4-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="68ad4-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68ad4-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68ad4-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68ad4-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68ad4-152">PROVIDERSPECIFICINPUT: <IReplicationProviderSpecificContainerMappingInput> 페어링에 대한 공급자 특정 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="68ad4-153">`[InstanceType <String>]`: 클래스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="68ad4-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="68ad4-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68ad4-154">RELATED LINKS</span></span>

