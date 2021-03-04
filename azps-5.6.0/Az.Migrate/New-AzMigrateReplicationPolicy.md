---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 7f9b78a6c287f7135f2463a6cfe63b2963ffe362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982672"
---
# <span data-ttu-id="aac28-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="aac28-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="aac28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac28-102">SYNOPSIS</span></span>
<span data-ttu-id="aac28-103">복제 정책을 만드는 작업</span><span class="sxs-lookup"><span data-stu-id="aac28-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="aac28-104">구문</span><span class="sxs-lookup"><span data-stu-id="aac28-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aac28-105">설명</span><span class="sxs-lookup"><span data-stu-id="aac28-105">DESCRIPTION</span></span>
<span data-ttu-id="aac28-106">복제 정책을 만드는 작업</span><span class="sxs-lookup"><span data-stu-id="aac28-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="aac28-107">예제</span><span class="sxs-lookup"><span data-stu-id="aac28-107">EXAMPLES</span></span>

### <span data-ttu-id="aac28-108">예제 1: 복제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="aac28-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="aac28-109">VmWare Cbt에 대한 정책 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="aac28-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aac28-110">PARAMETERS</span></span>

### <span data-ttu-id="aac28-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aac28-111">-AsJob</span></span>
<span data-ttu-id="aac28-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-112">Run the command as a job</span></span>

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

### <span data-ttu-id="aac28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac28-113">-DefaultProfile</span></span>
<span data-ttu-id="aac28-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac28-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aac28-115">-NoWait</span></span>
<span data-ttu-id="aac28-116">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="aac28-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aac28-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="aac28-117">-PolicyName</span></span>
<span data-ttu-id="aac28-118">복제 정책 이름</span><span class="sxs-lookup"><span data-stu-id="aac28-118">Replication policy name</span></span>

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

### <span data-ttu-id="aac28-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="aac28-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="aac28-120">복제ProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="aac28-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="aac28-121">생성을 위해 PROVIDERSPECIFICINPUT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="aac28-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac28-122">-ResourceGroupName</span></span>
<span data-ttu-id="aac28-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="aac28-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aac28-124">-ResourceName</span></span>
<span data-ttu-id="aac28-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="aac28-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aac28-126">-SubscriptionId</span></span>
<span data-ttu-id="aac28-127">프로젝트를 마이그레이션하는 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="aac28-128">-확인</span><span class="sxs-lookup"><span data-stu-id="aac28-128">-Confirm</span></span>
<span data-ttu-id="aac28-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac28-130">-WhatIf</span></span>
<span data-ttu-id="aac28-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac28-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac28-133">CommonParameters</span></span>
<span data-ttu-id="aac28-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac28-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aac28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac28-136">입력</span><span class="sxs-lookup"><span data-stu-id="aac28-136">INPUTS</span></span>

## <span data-ttu-id="aac28-137">출력</span><span class="sxs-lookup"><span data-stu-id="aac28-137">OUTPUTS</span></span>

### <span data-ttu-id="aac28-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="aac28-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="aac28-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aac28-139">NOTES</span></span>

<span data-ttu-id="aac28-140">별칭</span><span class="sxs-lookup"><span data-stu-id="aac28-140">ALIASES</span></span>

<span data-ttu-id="aac28-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="aac28-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aac28-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aac28-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aac28-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aac28-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : 복제ProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="aac28-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="aac28-145">`[InstanceType <String>]`: 클래스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="aac28-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="aac28-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aac28-146">RELATED LINKS</span></span>

