---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219022"
---
# <span data-ttu-id="d244d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d244d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="d244d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d244d-102">SYNOPSIS</span></span>
<span data-ttu-id="d244d-103">클러스터에 대 한 Kusto를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="d244d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d244d-104">SYNTAX</span></span>

### <span data-ttu-id="d244d-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d244d-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d244d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d244d-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d244d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d244d-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d244d-108">목록</span><span class="sxs-lookup"><span data-stu-id="d244d-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d244d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d244d-109">DESCRIPTION</span></span>
<span data-ttu-id="d244d-110">클러스터에 대 한 Kusto를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="d244d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d244d-111">EXAMPLES</span></span>

### <span data-ttu-id="d244d-112">예제 1: 리소스 그룹에 모든 Kusto 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="d244d-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="d244d-113">위의 명령은 리소스 그룹 "testrg"에 모든 Kusto 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="d244d-114">예제 2: 이름으로 특정 Kusto 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d244d-115">위의 명령은 리소스 그룹 "testrg"에서 "testnewkustocluster" 이라는 Kusto 클러스터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="d244d-116">변수</span><span class="sxs-lookup"><span data-stu-id="d244d-116">PARAMETERS</span></span>

### <span data-ttu-id="d244d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d244d-117">-DefaultProfile</span></span>
<span data-ttu-id="d244d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d244d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d244d-119">-InputObject</span></span>
<span data-ttu-id="d244d-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d244d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d244d-121">-Name</span></span>
<span data-ttu-id="d244d-122">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d244d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d244d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d244d-124">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d244d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d244d-125">-SubscriptionId</span></span>
<span data-ttu-id="d244d-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d244d-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d244d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d244d-128">CommonParameters</span></span>
<span data-ttu-id="d244d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d244d-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d244d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d244d-131">입력</span><span class="sxs-lookup"><span data-stu-id="d244d-131">INPUTS</span></span>

### <span data-ttu-id="d244d-132">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="d244d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d244d-133">출력</span><span class="sxs-lookup"><span data-stu-id="d244d-133">OUTPUTS</span></span>

### <span data-ttu-id="d244d-134">Microsoft. Api20200614. ICluster에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d244d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="d244d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d244d-135">NOTES</span></span>

<span data-ttu-id="d244d-136">별칭과</span><span class="sxs-lookup"><span data-stu-id="d244d-136">ALIASES</span></span>

<span data-ttu-id="d244d-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d244d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d244d-138">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d244d-139">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d244d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d244d-140">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d244d-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d244d-141">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d244d-142">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d244d-143">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d244d-144">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d244d-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d244d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d244d-146">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="d244d-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d244d-147">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d244d-148">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d244d-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d244d-150">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d244d-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d244d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d244d-151">RELATED LINKS</span></span>

