---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217715"
---
# <span data-ttu-id="c7f6c-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c7f6c-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="c7f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f6c-103">데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-103">Updates a database.</span></span>

## <span data-ttu-id="c7f6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7f6c-104">SYNTAX</span></span>

### <span data-ttu-id="c7f6c-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7f6c-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7f6c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7f6c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7f6c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c7f6c-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f6c-108">데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-108">Updates a database.</span></span>

## <span data-ttu-id="c7f6c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c7f6c-109">EXAMPLES</span></span>

### <span data-ttu-id="c7f6c-110">예제 1: 이름으로 기존 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="c7f6c-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c7f6c-111">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"에서 "mykustodatabase"에 대 한 소프트 삭제 기간 및 과열 캐시 기간을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c7f6c-112">예제 2: id를 통해 기존 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="c7f6c-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c7f6c-113">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"에서 "mykustodatabase"에 대 한 소프트 삭제 기간 및 과열 캐시 기간을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c7f6c-114">예제 3: 이름으로 기존 읽기 전용 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="c7f6c-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c7f6c-115">위 명령은 리소스 그룹 "testrg"에 있는 클러스터 "myfollowercluster"의 Kusto 검색 기간을 "mykustodatabase" 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c7f6c-116">예제 4: id를 통해 기존 읽기 전용 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="c7f6c-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c7f6c-117">위 명령은 리소스 그룹 "testrg"에 있는 클러스터 "myfollowercluster"의 Kusto 검색 기간을 "mykustodatabase" 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c7f6c-118">변수</span><span class="sxs-lookup"><span data-stu-id="c7f6c-118">PARAMETERS</span></span>

### <span data-ttu-id="c7f6c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7f6c-119">-AsJob</span></span>
<span data-ttu-id="c7f6c-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c7f6c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="c7f6c-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c7f6c-121">-ClusterName</span></span>
<span data-ttu-id="c7f6c-122">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c7f6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f6c-123">-DefaultProfile</span></span>
<span data-ttu-id="c7f6c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7f6c-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="c7f6c-125">-HotCachePeriod</span></span>
<span data-ttu-id="c7f6c-126">TimeSpan에서 빠른 쿼리를 위해 캐시에 데이터를 유지 해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="c7f6c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7f6c-127">-InputObject</span></span>
<span data-ttu-id="c7f6c-128">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7f6c-129">-종류</span><span class="sxs-lookup"><span data-stu-id="c7f6c-129">-Kind</span></span>
<span data-ttu-id="c7f6c-130">데이터베이스의 종류</span><span class="sxs-lookup"><span data-stu-id="c7f6c-130">Kind of the database</span></span>

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

### <span data-ttu-id="c7f6c-131">-위치</span><span class="sxs-lookup"><span data-stu-id="c7f6c-131">-Location</span></span>
<span data-ttu-id="c7f6c-132">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-132">Resource location.</span></span>

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

### <span data-ttu-id="c7f6c-133">-이름</span><span class="sxs-lookup"><span data-stu-id="c7f6c-133">-Name</span></span>
<span data-ttu-id="c7f6c-134">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c7f6c-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c7f6c-135">-NoWait</span></span>
<span data-ttu-id="c7f6c-136">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c7f6c-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c7f6c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f6c-137">-ResourceGroupName</span></span>
<span data-ttu-id="c7f6c-138">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c7f6c-139">-소프트 Deleteperiod</span><span class="sxs-lookup"><span data-stu-id="c7f6c-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="c7f6c-140">TimeSpan의 쿼리에 액세스할 수 있으려면 먼저 데이터를 유지 해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="c7f6c-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7f6c-141">-SubscriptionId</span></span>
<span data-ttu-id="c7f6c-142">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c7f6c-143">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c7f6c-144">-확인</span><span class="sxs-lookup"><span data-stu-id="c7f6c-144">-Confirm</span></span>
<span data-ttu-id="c7f6c-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f6c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f6c-146">-WhatIf</span></span>
<span data-ttu-id="c7f6c-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f6c-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f6c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f6c-149">CommonParameters</span></span>
<span data-ttu-id="c7f6c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f6c-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f6c-152">입력</span><span class="sxs-lookup"><span data-stu-id="c7f6c-152">INPUTS</span></span>

### <span data-ttu-id="c7f6c-153">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="c7f6c-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c7f6c-154">출력</span><span class="sxs-lookup"><span data-stu-id="c7f6c-154">OUTPUTS</span></span>

### <span data-ttu-id="c7f6c-155">Microsoft. Api20200614 데이터베이스에 대 한 자세한 모든.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="c7f6c-156">상속자</span><span class="sxs-lookup"><span data-stu-id="c7f6c-156">NOTES</span></span>

<span data-ttu-id="c7f6c-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="c7f6c-157">ALIASES</span></span>

<span data-ttu-id="c7f6c-158">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c7f6c-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7f6c-159">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7f6c-160">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7f6c-161">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7f6c-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7f6c-162">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c7f6c-163">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c7f6c-164">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c7f6c-165">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c7f6c-166">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c7f6c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7f6c-167">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c7f6c-168">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c7f6c-169">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c7f6c-170">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c7f6c-171">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f6c-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c7f6c-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7f6c-172">RELATED LINKS</span></span>

