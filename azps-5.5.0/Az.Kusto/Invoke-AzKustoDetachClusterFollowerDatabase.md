---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209269"
---
# <span data-ttu-id="8b0de-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="8b0de-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="8b0de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b0de-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0de-103">이 클러스터가 소유한 데이터베이스의 모든 팔로워를 디스어체합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="8b0de-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b0de-104">SYNTAX</span></span>

### <span data-ttu-id="8b0de-105">DetachExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="8b0de-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b0de-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8b0de-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b0de-107">설명</span><span class="sxs-lookup"><span data-stu-id="8b0de-107">DESCRIPTION</span></span>
<span data-ttu-id="8b0de-108">이 클러스터가 소유한 데이터베이스의 모든 팔로워를 디스어체합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="8b0de-109">예제</span><span class="sxs-lookup"><span data-stu-id="8b0de-109">EXAMPLES</span></span>

### <span data-ttu-id="8b0de-110">예제 1: 팔로워 데이터베이스 연결 다</span><span class="sxs-lookup"><span data-stu-id="8b0de-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="8b0de-111">위의 명령은 AttachedDatabaseConfiguration "myfollowerconfiguration"에 정의된 팔로워 데이터베이스를 클러스터 "testnewkustoclusterf"에서 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="8b0de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b0de-112">PARAMETERS</span></span>

### <span data-ttu-id="8b0de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b0de-113">-AsJob</span></span>
<span data-ttu-id="8b0de-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="8b0de-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8b0de-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8b0de-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="8b0de-116">팔로워 클러스터에 연결된 데이터베이스 구성의 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="8b0de-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8b0de-117">-ClusterName</span></span>
<span data-ttu-id="8b0de-118">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8b0de-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="8b0de-119">-ClusterResourceId</span></span>
<span data-ttu-id="8b0de-120">이 클러스터가 소유한 데이터베이스를 따르는 클러스터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="8b0de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0de-121">-DefaultProfile</span></span>
<span data-ttu-id="8b0de-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b0de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b0de-123">-InputObject</span></span>
<span data-ttu-id="8b0de-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8b0de-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8b0de-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8b0de-125">-NoWait</span></span>
<span data-ttu-id="8b0de-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="8b0de-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b0de-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b0de-127">-PassThru</span></span>
<span data-ttu-id="8b0de-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8b0de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0de-129">-ResourceGroupName</span></span>
<span data-ttu-id="8b0de-130">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8b0de-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b0de-131">-SubscriptionId</span></span>
<span data-ttu-id="8b0de-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b0de-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8b0de-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b0de-134">-Confirm</span></span>
<span data-ttu-id="8b0de-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0de-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0de-136">-WhatIf</span></span>
<span data-ttu-id="8b0de-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8b0de-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0de-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0de-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0de-139">CommonParameters</span></span>
<span data-ttu-id="8b0de-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0de-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b0de-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0de-142">입력</span><span class="sxs-lookup"><span data-stu-id="8b0de-142">INPUTS</span></span>

### <span data-ttu-id="8b0de-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8b0de-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8b0de-144">출력</span><span class="sxs-lookup"><span data-stu-id="8b0de-144">OUTPUTS</span></span>

### <span data-ttu-id="8b0de-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b0de-145">System.Boolean</span></span>

## <span data-ttu-id="8b0de-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b0de-146">NOTES</span></span>

<span data-ttu-id="8b0de-147">별칭</span><span class="sxs-lookup"><span data-stu-id="8b0de-147">ALIASES</span></span>

<span data-ttu-id="8b0de-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8b0de-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b0de-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b0de-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b0de-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b0de-151">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b0de-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b0de-152">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8b0de-153">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8b0de-154">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8b0de-155">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8b0de-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8b0de-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b0de-157">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8b0de-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8b0de-159">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8b0de-160">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8b0de-161">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8b0de-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8b0de-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b0de-162">RELATED LINKS</span></span>
