---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: b7638780dc4fa360998d7d974d74c93ccd5c2afe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180417"
---
# <span data-ttu-id="ab7c4-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ab7c4-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="ab7c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7c4-103">데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-103">Updates a database.</span></span>

## <span data-ttu-id="ab7c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab7c4-104">SYNTAX</span></span>

### <span data-ttu-id="ab7c4-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab7c4-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab7c4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ab7c4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab7c4-107">설명</span><span class="sxs-lookup"><span data-stu-id="ab7c4-107">DESCRIPTION</span></span>
<span data-ttu-id="ab7c4-108">데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-108">Updates a database.</span></span>

## <span data-ttu-id="ab7c4-109">예제</span><span class="sxs-lookup"><span data-stu-id="ab7c4-109">EXAMPLES</span></span>

### <span data-ttu-id="ab7c4-110">예제 1: 이름에 따라 기존 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="ab7c4-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ab7c4-111">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"에서 Kusto 데이터베이스 "mykustodatabase"의 소프트 삭제 기간 및 핫 캐시 기간을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ab7c4-112">예제 2: ID를 통해 기존 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="ab7c4-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ab7c4-113">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"에서 Kusto 데이터베이스 "mykustodatabase"의 소프트 삭제 기간 및 핫 캐시 기간을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ab7c4-114">예제 3: 이름에 따라 기존 ReadOnly 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="ab7c4-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ab7c4-115">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "myfollowercluster"에서 Kusto 데이터베이스 "mykustodatabase"의 핫 캐시 기간을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ab7c4-116">예제 4: ID를 통해 기존 ReadOnly 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="ab7c4-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ab7c4-117">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "myfollowercluster"에서 Kusto 데이터베이스 "mykustodatabase"의 핫 캐시 기간을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="ab7c4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab7c4-118">PARAMETERS</span></span>

### <span data-ttu-id="ab7c4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab7c4-119">-AsJob</span></span>
<span data-ttu-id="ab7c4-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ab7c4-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ab7c4-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ab7c4-121">-ClusterName</span></span>
<span data-ttu-id="ab7c4-122">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7c4-123">-DefaultProfile</span></span>
<span data-ttu-id="ab7c4-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab7c4-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="ab7c4-125">-HotCachePeriod</span></span>
<span data-ttu-id="ab7c4-126">TimeSpan에서 빠른 쿼리를 위해 데이터를 캐시에 보관해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab7c4-127">-InputObject</span></span>
<span data-ttu-id="ab7c4-128">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="ab7c4-129">-Kind</span></span>
<span data-ttu-id="ab7c4-130">데이터베이스의 종류</span><span class="sxs-lookup"><span data-stu-id="ab7c4-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-131">-Location</span><span class="sxs-lookup"><span data-stu-id="ab7c4-131">-Location</span></span>
<span data-ttu-id="ab7c4-132">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-132">Resource location.</span></span>

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

### <span data-ttu-id="ab7c4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ab7c4-133">-Name</span></span>
<span data-ttu-id="ab7c4-134">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ab7c4-135">-NoWait</span></span>
<span data-ttu-id="ab7c4-136">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ab7c4-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ab7c4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab7c4-137">-ResourceGroupName</span></span>
<span data-ttu-id="ab7c4-138">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="ab7c4-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="ab7c4-140">TimeSpan의 쿼리에 대한 액세스가 중지되기 전에 데이터를 유지해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab7c4-141">-SubscriptionId</span></span>
<span data-ttu-id="ab7c4-142">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab7c4-143">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab7c4-144">-Confirm</span></span>
<span data-ttu-id="ab7c4-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab7c4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab7c4-146">-WhatIf</span></span>
<span data-ttu-id="ab7c4-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ab7c4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab7c4-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab7c4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7c4-149">CommonParameters</span></span>
<span data-ttu-id="ab7c4-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7c4-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7c4-152">입력</span><span class="sxs-lookup"><span data-stu-id="ab7c4-152">INPUTS</span></span>

### <span data-ttu-id="ab7c4-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ab7c4-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ab7c4-154">출력</span><span class="sxs-lookup"><span data-stu-id="ab7c4-154">OUTPUTS</span></span>

### <span data-ttu-id="ab7c4-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="ab7c4-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="ab7c4-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab7c4-156">NOTES</span></span>

<span data-ttu-id="ab7c4-157">별칭</span><span class="sxs-lookup"><span data-stu-id="ab7c4-157">ALIASES</span></span>

<span data-ttu-id="ab7c4-158">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ab7c4-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab7c4-159">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab7c4-160">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab7c4-161">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ab7c4-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab7c4-162">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ab7c4-163">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ab7c4-164">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ab7c4-165">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ab7c4-166">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ab7c4-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab7c4-167">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ab7c4-168">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ab7c4-169">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ab7c4-170">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ab7c4-171">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab7c4-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ab7c4-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab7c4-172">RELATED LINKS</span></span>

