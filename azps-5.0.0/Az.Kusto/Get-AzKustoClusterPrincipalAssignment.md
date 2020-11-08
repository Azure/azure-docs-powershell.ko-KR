---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219017"
---
# <span data-ttu-id="3f5dd-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="3f5dd-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="3f5dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5dd-103">클러스터 principalAssignment에 대 한 Kusto를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="3f5dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f5dd-104">SYNTAX</span></span>

### <span data-ttu-id="3f5dd-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f5dd-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f5dd-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="3f5dd-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f5dd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f5dd-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f5dd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3f5dd-108">DESCRIPTION</span></span>
<span data-ttu-id="3f5dd-109">클러스터 principalAssignment에 대 한 Kusto를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="3f5dd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3f5dd-110">EXAMPLES</span></span>

### <span data-ttu-id="3f5dd-111">예제 1: 모든 Kusto principalAssignment 할당</span><span class="sxs-lookup"><span data-stu-id="3f5dd-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="3f5dd-112">위 명령은 "testnewkustocluster" 클러스터의 모든 principalAssignment을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3f5dd-113">예제 2: 이름으로 Kusto 클러스터 principalAssignment을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="3f5dd-114">위 명령에서는 "testnewkustocluster" 클러스터에 "kustoprincipal1" 이라는 Kusto 클러스터 principalAssignment를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="3f5dd-115">변수</span><span class="sxs-lookup"><span data-stu-id="3f5dd-115">PARAMETERS</span></span>

### <span data-ttu-id="3f5dd-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3f5dd-116">-ClusterName</span></span>
<span data-ttu-id="3f5dd-117">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3f5dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5dd-118">-DefaultProfile</span></span>
<span data-ttu-id="3f5dd-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f5dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f5dd-120">-InputObject</span></span>
<span data-ttu-id="3f5dd-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f5dd-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="3f5dd-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="3f5dd-123">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="3f5dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f5dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f5dd-125">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3f5dd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f5dd-126">-SubscriptionId</span></span>
<span data-ttu-id="3f5dd-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f5dd-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f5dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5dd-129">CommonParameters</span></span>
<span data-ttu-id="3f5dd-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5dd-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5dd-132">입력</span><span class="sxs-lookup"><span data-stu-id="3f5dd-132">INPUTS</span></span>

### <span data-ttu-id="3f5dd-133">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="3f5dd-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3f5dd-134">출력</span><span class="sxs-lookup"><span data-stu-id="3f5dd-134">OUTPUTS</span></span>

### <span data-ttu-id="3f5dd-135">Microsoft. Api20200614. IClusterPrincipalAssignment에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="3f5dd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3f5dd-136">NOTES</span></span>

<span data-ttu-id="3f5dd-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="3f5dd-137">ALIASES</span></span>

<span data-ttu-id="3f5dd-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3f5dd-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f5dd-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f5dd-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f5dd-141">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f5dd-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f5dd-142">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3f5dd-143">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3f5dd-144">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3f5dd-145">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3f5dd-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="3f5dd-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f5dd-147">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3f5dd-148">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3f5dd-149">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3f5dd-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3f5dd-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f5dd-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3f5dd-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f5dd-152">RELATED LINKS</span></span>

