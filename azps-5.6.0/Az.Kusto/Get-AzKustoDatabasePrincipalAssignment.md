---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 038db26826c4f3f37dcba42e1ccd435512ecd88b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986804"
---
# <span data-ttu-id="9608f-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9608f-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="9608f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9608f-102">SYNOPSIS</span></span>
<span data-ttu-id="9608f-103">Kusto 클러스터 데이터베이스 주체인Assignment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="9608f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9608f-104">SYNTAX</span></span>

### <span data-ttu-id="9608f-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="9608f-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9608f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9608f-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9608f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9608f-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9608f-108">설명</span><span class="sxs-lookup"><span data-stu-id="9608f-108">DESCRIPTION</span></span>
<span data-ttu-id="9608f-109">Kusto 클러스터 데이터베이스 주체인Assignment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="9608f-110">예제</span><span class="sxs-lookup"><span data-stu-id="9608f-110">EXAMPLES</span></span>

### <span data-ttu-id="9608f-111">예제 1: 데이터베이스에 이름에 따라 모든 PrincipalAssignment 나열</span><span class="sxs-lookup"><span data-stu-id="9608f-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="9608f-112">위의 명령은 "testnewkustocluster"에 있는 데이터베이스 "mykustodatabase"의 모든 PrincipalAssignment를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9608f-113">예제 2: 이름별 데이터베이스에서 특정 PrincipalAssignment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="9608f-114">위의 명령은 "testnewkustocluster"에 있는 데이터베이스 "mykustodatabase"에서 "kustoprincipal1"이라는 모든 PrincipalAssignment를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9608f-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9608f-115">PARAMETERS</span></span>

### <span data-ttu-id="9608f-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9608f-116">-ClusterName</span></span>
<span data-ttu-id="9608f-117">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9608f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9608f-118">-DatabaseName</span></span>
<span data-ttu-id="9608f-119">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="9608f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9608f-120">-DefaultProfile</span></span>
<span data-ttu-id="9608f-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9608f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9608f-122">-InputObject</span></span>
<span data-ttu-id="9608f-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9608f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9608f-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9608f-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="9608f-125">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9608f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9608f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9608f-127">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9608f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9608f-128">-SubscriptionId</span></span>
<span data-ttu-id="9608f-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9608f-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9608f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9608f-131">CommonParameters</span></span>
<span data-ttu-id="9608f-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9608f-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9608f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9608f-134">입력</span><span class="sxs-lookup"><span data-stu-id="9608f-134">INPUTS</span></span>

### <span data-ttu-id="9608f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9608f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9608f-136">출력</span><span class="sxs-lookup"><span data-stu-id="9608f-136">OUTPUTS</span></span>

### <span data-ttu-id="9608f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9608f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="9608f-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9608f-138">NOTES</span></span>

<span data-ttu-id="9608f-139">별칭</span><span class="sxs-lookup"><span data-stu-id="9608f-139">ALIASES</span></span>

<span data-ttu-id="9608f-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9608f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9608f-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9608f-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9608f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9608f-143">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9608f-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9608f-144">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9608f-145">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9608f-146">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9608f-147">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9608f-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="9608f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9608f-149">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9608f-150">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9608f-151">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9608f-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9608f-153">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="9608f-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9608f-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9608f-154">RELATED LINKS</span></span>

