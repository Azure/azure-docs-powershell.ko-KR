---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219001"
---
# <span data-ttu-id="d0332-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="d0332-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="d0332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0332-102">SYNOPSIS</span></span>
<span data-ttu-id="d0332-103">이 클러스터가 소유한 데이터베이스의 모든 팔을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="d0332-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0332-104">SYNTAX</span></span>

### <span data-ttu-id="d0332-105">DetachExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0332-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0332-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d0332-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0332-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d0332-107">DESCRIPTION</span></span>
<span data-ttu-id="d0332-108">이 클러스터가 소유한 데이터베이스의 모든 팔을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="d0332-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d0332-109">EXAMPLES</span></span>

### <span data-ttu-id="d0332-110">예제 1: 종동체 데이터베이스 분리</span><span class="sxs-lookup"><span data-stu-id="d0332-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="d0332-111">위 명령으로 "AttachedDatabaseConfiguration" my</c13> 구성 "에서 정의 된 종동체 데이터베이스를 클러스터" testnewkustoclusterf "에서 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="d0332-112">변수</span><span class="sxs-lookup"><span data-stu-id="d0332-112">PARAMETERS</span></span>

### <span data-ttu-id="d0332-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0332-113">-AsJob</span></span>
<span data-ttu-id="d0332-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0332-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d0332-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d0332-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="d0332-116">종동체 클러스터의 연결 된 데이터베이스 구성의 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="d0332-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d0332-117">-ClusterName</span></span>
<span data-ttu-id="d0332-118">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0332-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="d0332-119">-ClusterResourceId</span></span>
<span data-ttu-id="d0332-120">이 클러스터가 소유 하는 데이터베이스를 팔 로우 하는 클러스터의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="d0332-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0332-121">-DefaultProfile</span></span>
<span data-ttu-id="d0332-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0332-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0332-123">-InputObject</span></span>
<span data-ttu-id="d0332-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0332-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0332-125">-NoWait</span></span>
<span data-ttu-id="d0332-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0332-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0332-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0332-127">-PassThru</span></span>
<span data-ttu-id="d0332-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d0332-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0332-129">-ResourceGroupName</span></span>
<span data-ttu-id="d0332-130">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0332-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0332-131">-SubscriptionId</span></span>
<span data-ttu-id="d0332-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0332-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0332-134">-확인</span><span class="sxs-lookup"><span data-stu-id="d0332-134">-Confirm</span></span>
<span data-ttu-id="d0332-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0332-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0332-136">-WhatIf</span></span>
<span data-ttu-id="d0332-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0332-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0332-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0332-139">CommonParameters</span></span>
<span data-ttu-id="d0332-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0332-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0332-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0332-142">입력</span><span class="sxs-lookup"><span data-stu-id="d0332-142">INPUTS</span></span>

### <span data-ttu-id="d0332-143">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="d0332-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d0332-144">출력</span><span class="sxs-lookup"><span data-stu-id="d0332-144">OUTPUTS</span></span>

### <span data-ttu-id="d0332-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d0332-145">System.Boolean</span></span>

## <span data-ttu-id="d0332-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d0332-146">NOTES</span></span>

<span data-ttu-id="d0332-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="d0332-147">ALIASES</span></span>

<span data-ttu-id="d0332-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d0332-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0332-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0332-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0332-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0332-151">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0332-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0332-152">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d0332-153">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d0332-154">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d0332-155">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d0332-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d0332-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0332-157">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="d0332-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d0332-158">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d0332-159">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d0332-160">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d0332-161">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0332-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d0332-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0332-162">RELATED LINKS</span></span>

