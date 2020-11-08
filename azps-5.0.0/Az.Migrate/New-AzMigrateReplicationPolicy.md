---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217315"
---
# <span data-ttu-id="31b62-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="31b62-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="31b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b62-102">SYNOPSIS</span></span>
<span data-ttu-id="31b62-103">복제 정책 만들기 작업</span><span class="sxs-lookup"><span data-stu-id="31b62-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="31b62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31b62-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31b62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31b62-105">DESCRIPTION</span></span>
<span data-ttu-id="31b62-106">복제 정책 만들기 작업</span><span class="sxs-lookup"><span data-stu-id="31b62-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="31b62-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31b62-107">EXAMPLES</span></span>

### <span data-ttu-id="31b62-108">예제 1: 복제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="31b62-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="31b62-109">VmWare Cbt에 대 한 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="31b62-110">변수</span><span class="sxs-lookup"><span data-stu-id="31b62-110">PARAMETERS</span></span>

### <span data-ttu-id="31b62-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31b62-111">-AsJob</span></span>
<span data-ttu-id="31b62-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="31b62-112">Run the command as a job</span></span>

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

### <span data-ttu-id="31b62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b62-113">-DefaultProfile</span></span>
<span data-ttu-id="31b62-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b62-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="31b62-115">-NoWait</span></span>
<span data-ttu-id="31b62-116">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="31b62-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="31b62-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="31b62-117">-PolicyName</span></span>
<span data-ttu-id="31b62-118">복제 정책 이름</span><span class="sxs-lookup"><span data-stu-id="31b62-118">Replication policy name</span></span>

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

### <span data-ttu-id="31b62-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="31b62-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="31b62-120">ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="31b62-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="31b62-121">생성 하려면 PROVIDERSPECIFICINPUT 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="31b62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b62-122">-ResourceGroupName</span></span>
<span data-ttu-id="31b62-123">복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="31b62-124">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="31b62-124">-ResourceName</span></span>
<span data-ttu-id="31b62-125">복구 서비스 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="31b62-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31b62-126">-SubscriptionId</span></span>
<span data-ttu-id="31b62-127">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-127">The subscription Id.</span></span>

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

### <span data-ttu-id="31b62-128">-확인</span><span class="sxs-lookup"><span data-stu-id="31b62-128">-Confirm</span></span>
<span data-ttu-id="31b62-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b62-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b62-130">-WhatIf</span></span>
<span data-ttu-id="31b62-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b62-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b62-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b62-133">CommonParameters</span></span>
<span data-ttu-id="31b62-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b62-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31b62-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b62-136">입력</span><span class="sxs-lookup"><span data-stu-id="31b62-136">INPUTS</span></span>

## <span data-ttu-id="31b62-137">출력</span><span class="sxs-lookup"><span data-stu-id="31b62-137">OUTPUTS</span></span>

### <span data-ttu-id="31b62-138">Api20180110 (Microsoft. PowerShell. .exe 정책)</span><span class="sxs-lookup"><span data-stu-id="31b62-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="31b62-139">상속자</span><span class="sxs-lookup"><span data-stu-id="31b62-139">NOTES</span></span>

<span data-ttu-id="31b62-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="31b62-140">ALIASES</span></span>

<span data-ttu-id="31b62-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="31b62-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31b62-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31b62-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="31b62-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31b62-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="31b62-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="31b62-145">`[InstanceType <String>]`: 클래스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="31b62-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="31b62-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31b62-146">RELATED LINKS</span></span>

