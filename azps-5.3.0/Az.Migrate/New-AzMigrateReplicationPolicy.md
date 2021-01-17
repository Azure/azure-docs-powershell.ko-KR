---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489375"
---
# <span data-ttu-id="cae22-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cae22-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="cae22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae22-102">SYNOPSIS</span></span>
<span data-ttu-id="cae22-103">복제 정책을 만드는 작업</span><span class="sxs-lookup"><span data-stu-id="cae22-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="cae22-104">구문</span><span class="sxs-lookup"><span data-stu-id="cae22-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cae22-105">설명</span><span class="sxs-lookup"><span data-stu-id="cae22-105">DESCRIPTION</span></span>
<span data-ttu-id="cae22-106">복제 정책을 만드는 작업</span><span class="sxs-lookup"><span data-stu-id="cae22-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="cae22-107">예제</span><span class="sxs-lookup"><span data-stu-id="cae22-107">EXAMPLES</span></span>

### <span data-ttu-id="cae22-108">예제 1: 복제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="cae22-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="cae22-109">VmWare Cbt에 대한 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="cae22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae22-110">PARAMETERS</span></span>

### <span data-ttu-id="cae22-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cae22-111">-AsJob</span></span>
<span data-ttu-id="cae22-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="cae22-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cae22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae22-113">-DefaultProfile</span></span>
<span data-ttu-id="cae22-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cae22-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cae22-115">-NoWait</span></span>
<span data-ttu-id="cae22-116">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="cae22-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cae22-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="cae22-117">-PolicyName</span></span>
<span data-ttu-id="cae22-118">복제 정책 이름</span><span class="sxs-lookup"><span data-stu-id="cae22-118">Replication policy name</span></span>

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

### <span data-ttu-id="cae22-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="cae22-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="cae22-120">The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="cae22-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="cae22-121">생성을 위해 PROVIDERSPECIFICINPUT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cae22-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cae22-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae22-122">-ResourceGroupName</span></span>
<span data-ttu-id="cae22-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="cae22-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cae22-124">-ResourceName</span></span>
<span data-ttu-id="cae22-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="cae22-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cae22-126">-SubscriptionId</span></span>
<span data-ttu-id="cae22-127">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-127">The subscription Id.</span></span>

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

### <span data-ttu-id="cae22-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cae22-128">-Confirm</span></span>
<span data-ttu-id="cae22-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae22-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae22-130">-WhatIf</span></span>
<span data-ttu-id="cae22-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cae22-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae22-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae22-133">CommonParameters</span></span>
<span data-ttu-id="cae22-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae22-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cae22-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae22-136">입력</span><span class="sxs-lookup"><span data-stu-id="cae22-136">INPUTS</span></span>

## <span data-ttu-id="cae22-137">출력</span><span class="sxs-lookup"><span data-stu-id="cae22-137">OUTPUTS</span></span>

### <span data-ttu-id="cae22-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="cae22-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="cae22-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cae22-139">NOTES</span></span>

<span data-ttu-id="cae22-140">별칭</span><span class="sxs-lookup"><span data-stu-id="cae22-140">ALIASES</span></span>

<span data-ttu-id="cae22-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cae22-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cae22-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cae22-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cae22-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cae22-144">PROVIDERSPECIFICINPUT: <IPolicyProviderSpecificInput> ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="cae22-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="cae22-145">`[InstanceType <String>]`: 클래스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cae22-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="cae22-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cae22-146">RELATED LINKS</span></span>

