---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218635"
---
# <span data-ttu-id="746ce-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="746ce-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="746ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="746ce-102">SYNOPSIS</span></span>
<span data-ttu-id="746ce-103">보호 컨테이너 매핑을 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="746ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="746ce-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="746ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="746ce-105">DESCRIPTION</span></span>
<span data-ttu-id="746ce-106">보호 컨테이너 매핑을 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="746ce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="746ce-107">EXAMPLES</span></span>

### <span data-ttu-id="746ce-108">예제 1: 매핑 만들기</span><span class="sxs-lookup"><span data-stu-id="746ce-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="746ce-109">매핑 만들기</span><span class="sxs-lookup"><span data-stu-id="746ce-109">Create a mapping</span></span>

## <span data-ttu-id="746ce-110">변수</span><span class="sxs-lookup"><span data-stu-id="746ce-110">PARAMETERS</span></span>

### <span data-ttu-id="746ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="746ce-111">-AsJob</span></span>
<span data-ttu-id="746ce-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="746ce-112">Run the command as a job</span></span>

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

### <span data-ttu-id="746ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746ce-113">-DefaultProfile</span></span>
<span data-ttu-id="746ce-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746ce-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="746ce-115">-FabricName</span></span>
<span data-ttu-id="746ce-116">패브릭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-116">Fabric name.</span></span>

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

### <span data-ttu-id="746ce-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="746ce-117">-MappingName</span></span>
<span data-ttu-id="746ce-118">보호 컨테이너 매핑 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="746ce-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="746ce-119">-NoWait</span></span>
<span data-ttu-id="746ce-120">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="746ce-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="746ce-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="746ce-121">-PolicyId</span></span>
<span data-ttu-id="746ce-122">해당 정책</span><span class="sxs-lookup"><span data-stu-id="746ce-122">Applicable policy.</span></span>

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

### <span data-ttu-id="746ce-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="746ce-123">-ProtectionContainerName</span></span>
<span data-ttu-id="746ce-124">보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-124">Protection container name.</span></span>

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

### <span data-ttu-id="746ce-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="746ce-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="746ce-126">페어링에 대 한 공급자별 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="746ce-127">생성 하려면 PROVIDERSPECIFICINPUT 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="746ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="746ce-129">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="746ce-130">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="746ce-130">-ResourceName</span></span>
<span data-ttu-id="746ce-131">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="746ce-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="746ce-132">-SubscriptionId</span></span>
<span data-ttu-id="746ce-133">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-133">The subscription Id.</span></span>

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

### <span data-ttu-id="746ce-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="746ce-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="746ce-135">대상 고유 보호 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="746ce-136">-확인</span><span class="sxs-lookup"><span data-stu-id="746ce-136">-Confirm</span></span>
<span data-ttu-id="746ce-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746ce-138">-WhatIf</span></span>
<span data-ttu-id="746ce-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746ce-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746ce-141">CommonParameters</span></span>
<span data-ttu-id="746ce-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746ce-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="746ce-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746ce-144">입력</span><span class="sxs-lookup"><span data-stu-id="746ce-144">INPUTS</span></span>

## <span data-ttu-id="746ce-145">출력</span><span class="sxs-lookup"><span data-stu-id="746ce-145">OUTPUTS</span></span>

### <span data-ttu-id="746ce-146">Api20180110. IProtectionContainerMapping의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="746ce-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="746ce-147">상속자</span><span class="sxs-lookup"><span data-stu-id="746ce-147">NOTES</span></span>

<span data-ttu-id="746ce-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="746ce-148">ALIASES</span></span>

<span data-ttu-id="746ce-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="746ce-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="746ce-150">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="746ce-151">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="746ce-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="746ce-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : 페어링에 대 한 공급자별 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="746ce-153">`[InstanceType <String>]`: 클래스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="746ce-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="746ce-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="746ce-154">RELATED LINKS</span></span>

