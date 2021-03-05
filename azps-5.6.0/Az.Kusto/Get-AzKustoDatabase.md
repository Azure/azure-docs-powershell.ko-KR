---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 714f971b32f9863ab2e5dc088d07859f2f5181a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964432"
---
# <span data-ttu-id="51793-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="51793-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="51793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51793-102">SYNOPSIS</span></span>
<span data-ttu-id="51793-103">데이터베이스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-103">Returns a database.</span></span>

## <span data-ttu-id="51793-104">구문</span><span class="sxs-lookup"><span data-stu-id="51793-104">SYNTAX</span></span>

### <span data-ttu-id="51793-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="51793-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51793-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="51793-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51793-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51793-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="51793-108">설명</span><span class="sxs-lookup"><span data-stu-id="51793-108">DESCRIPTION</span></span>
<span data-ttu-id="51793-109">데이터베이스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-109">Returns a database.</span></span>

## <span data-ttu-id="51793-110">예제</span><span class="sxs-lookup"><span data-stu-id="51793-110">EXAMPLES</span></span>

### <span data-ttu-id="51793-111">예제 1: 이름에 따라 클러스터의 모든 Kusto 데이터베이스 나열</span><span class="sxs-lookup"><span data-stu-id="51793-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="51793-112">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"의 모든 Kusto 데이터베이스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="51793-113">예제 2: 이름별 특정 Kusto 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51793-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="51793-114">위의 명령은 "testrg"에 있는 클러스터 "testnewkustocluster"에서 "mykustodatabase"라는 Kusto 데이터베이스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="51793-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51793-115">PARAMETERS</span></span>

### <span data-ttu-id="51793-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="51793-116">-ClusterName</span></span>
<span data-ttu-id="51793-117">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51793-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51793-118">-DefaultProfile</span></span>
<span data-ttu-id="51793-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51793-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51793-120">-InputObject</span></span>
<span data-ttu-id="51793-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="51793-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51793-122">-Name</span><span class="sxs-lookup"><span data-stu-id="51793-122">-Name</span></span>
<span data-ttu-id="51793-123">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51793-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51793-124">-ResourceGroupName</span></span>
<span data-ttu-id="51793-125">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-125">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51793-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51793-126">-SubscriptionId</span></span>
<span data-ttu-id="51793-127">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51793-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="51793-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51793-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51793-129">CommonParameters</span></span>
<span data-ttu-id="51793-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51793-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51793-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51793-132">입력</span><span class="sxs-lookup"><span data-stu-id="51793-132">INPUTS</span></span>

### <span data-ttu-id="51793-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="51793-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="51793-134">출력</span><span class="sxs-lookup"><span data-stu-id="51793-134">OUTPUTS</span></span>

### <span data-ttu-id="51793-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="51793-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="51793-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51793-136">NOTES</span></span>

<span data-ttu-id="51793-137">별칭</span><span class="sxs-lookup"><span data-stu-id="51793-137">ALIASES</span></span>

<span data-ttu-id="51793-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="51793-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51793-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51793-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51793-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51793-141">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="51793-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51793-142">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="51793-143">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="51793-144">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="51793-145">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="51793-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="51793-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51793-147">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="51793-148">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="51793-149">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51793-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="51793-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51793-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="51793-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="51793-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="51793-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51793-152">RELATED LINKS</span></span>

