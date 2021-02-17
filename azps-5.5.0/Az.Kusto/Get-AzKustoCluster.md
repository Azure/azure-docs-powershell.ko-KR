---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185289"
---
# <span data-ttu-id="cb259-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="cb259-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="cb259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb259-102">SYNOPSIS</span></span>
<span data-ttu-id="cb259-103">Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="cb259-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb259-104">SYNTAX</span></span>

### <span data-ttu-id="cb259-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb259-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb259-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="cb259-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb259-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb259-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb259-108">목록</span><span class="sxs-lookup"><span data-stu-id="cb259-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb259-109">설명</span><span class="sxs-lookup"><span data-stu-id="cb259-109">DESCRIPTION</span></span>
<span data-ttu-id="cb259-110">Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="cb259-111">예제</span><span class="sxs-lookup"><span data-stu-id="cb259-111">EXAMPLES</span></span>

### <span data-ttu-id="cb259-112">예제 1: 리소스 그룹의 모든 Kusto 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="cb259-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="cb259-113">위의 명령은 리소스 그룹 "testrg"의 모든 Kusto 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="cb259-114">예제 2: 이름으로 특정 Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="cb259-115">위의 명령은 리소스 그룹 "testrg"에서 "testnewkustocluster"라는 Kusto 클러스터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="cb259-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb259-116">PARAMETERS</span></span>

### <span data-ttu-id="cb259-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb259-117">-DefaultProfile</span></span>
<span data-ttu-id="cb259-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb259-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb259-119">-InputObject</span></span>
<span data-ttu-id="cb259-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cb259-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cb259-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cb259-121">-Name</span></span>
<span data-ttu-id="cb259-122">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb259-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb259-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb259-124">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cb259-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb259-125">-SubscriptionId</span></span>
<span data-ttu-id="cb259-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb259-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb259-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb259-128">CommonParameters</span></span>
<span data-ttu-id="cb259-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb259-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb259-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb259-131">입력</span><span class="sxs-lookup"><span data-stu-id="cb259-131">INPUTS</span></span>

### <span data-ttu-id="cb259-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cb259-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cb259-133">출력</span><span class="sxs-lookup"><span data-stu-id="cb259-133">OUTPUTS</span></span>

### <span data-ttu-id="cb259-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="cb259-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="cb259-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb259-135">NOTES</span></span>

<span data-ttu-id="cb259-136">별칭</span><span class="sxs-lookup"><span data-stu-id="cb259-136">ALIASES</span></span>

<span data-ttu-id="cb259-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cb259-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb259-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb259-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb259-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb259-140">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb259-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb259-141">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cb259-142">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cb259-143">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cb259-144">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cb259-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="cb259-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb259-146">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cb259-147">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cb259-148">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cb259-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb259-150">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cb259-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cb259-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb259-151">RELATED LINKS</span></span>

