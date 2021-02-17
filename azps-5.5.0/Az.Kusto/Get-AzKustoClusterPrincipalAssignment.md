---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185268"
---
# <span data-ttu-id="96173-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="96173-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="96173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96173-102">SYNOPSIS</span></span>
<span data-ttu-id="96173-103">Kusto 클러스터 principalAssignment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96173-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="96173-104">구문</span><span class="sxs-lookup"><span data-stu-id="96173-104">SYNTAX</span></span>

### <span data-ttu-id="96173-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="96173-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96173-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="96173-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96173-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96173-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="96173-108">설명</span><span class="sxs-lookup"><span data-stu-id="96173-108">DESCRIPTION</span></span>
<span data-ttu-id="96173-109">Kusto 클러스터 principalAssignment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96173-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="96173-110">예제</span><span class="sxs-lookup"><span data-stu-id="96173-110">EXAMPLES</span></span>

### <span data-ttu-id="96173-111">예제 1: 모든 Kusto 클러스터 principalAssignment 나열</span><span class="sxs-lookup"><span data-stu-id="96173-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="96173-112">위의 명령은 "testnewkustocluster" 클러스터의 모든 principalAssignment를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="96173-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="96173-113">예제 2: 이름으로 Kusto 클러스터 principalAssignment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96173-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="96173-114">위의 명령은 "testnewkustocluster" 클러스터에 "kustoprincipal1"이라는 Kusto 클러스터 principalAssignment를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="96173-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="96173-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96173-115">PARAMETERS</span></span>

### <span data-ttu-id="96173-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="96173-116">-ClusterName</span></span>
<span data-ttu-id="96173-117">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="96173-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96173-118">-DefaultProfile</span></span>
<span data-ttu-id="96173-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96173-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96173-120">-InputObject</span></span>
<span data-ttu-id="96173-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="96173-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96173-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="96173-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="96173-123">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="96173-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96173-124">-ResourceGroupName</span></span>
<span data-ttu-id="96173-125">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="96173-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96173-126">-SubscriptionId</span></span>
<span data-ttu-id="96173-127">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96173-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96173-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="96173-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96173-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96173-129">CommonParameters</span></span>
<span data-ttu-id="96173-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96173-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96173-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96173-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96173-132">입력</span><span class="sxs-lookup"><span data-stu-id="96173-132">INPUTS</span></span>

### <span data-ttu-id="96173-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="96173-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="96173-134">출력</span><span class="sxs-lookup"><span data-stu-id="96173-134">OUTPUTS</span></span>

### <span data-ttu-id="96173-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="96173-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="96173-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96173-136">NOTES</span></span>

<span data-ttu-id="96173-137">별칭</span><span class="sxs-lookup"><span data-stu-id="96173-137">ALIASES</span></span>

<span data-ttu-id="96173-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="96173-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96173-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="96173-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96173-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96173-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96173-141">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="96173-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96173-142">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="96173-143">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="96173-144">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="96173-145">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="96173-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="96173-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96173-147">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="96173-148">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="96173-149">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96173-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="96173-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96173-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="96173-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="96173-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="96173-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96173-152">RELATED LINKS</span></span>

