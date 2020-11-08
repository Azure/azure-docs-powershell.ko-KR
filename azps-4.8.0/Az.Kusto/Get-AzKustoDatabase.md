---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211855"
---
# <span data-ttu-id="c9a67-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c9a67-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="c9a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a67-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a67-103">데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-103">Returns a database.</span></span>

## <span data-ttu-id="c9a67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9a67-104">SYNTAX</span></span>

### <span data-ttu-id="c9a67-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c9a67-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9a67-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="c9a67-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9a67-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9a67-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9a67-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c9a67-108">DESCRIPTION</span></span>
<span data-ttu-id="c9a67-109">데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-109">Returns a database.</span></span>

## <span data-ttu-id="c9a67-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c9a67-110">EXAMPLES</span></span>

### <span data-ttu-id="c9a67-111">예제 1: 클러스터의 모든 Kname을 이름으로 하 여 데이터베이스에 나열</span><span class="sxs-lookup"><span data-stu-id="c9a67-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c9a67-112">위의 명령은 리소스 그룹 "testrg"에 있는 "testnewkustocluster" 클러스터의 모든 Kusto 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c9a67-113">예제 2: 이름으로 특정 Kusto 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9a67-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c9a67-114">위 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"에 있는 "mykustodatabase" 이라는 Kusto 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c9a67-115">변수</span><span class="sxs-lookup"><span data-stu-id="c9a67-115">PARAMETERS</span></span>

### <span data-ttu-id="c9a67-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c9a67-116">-ClusterName</span></span>
<span data-ttu-id="c9a67-117">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9a67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a67-118">-DefaultProfile</span></span>
<span data-ttu-id="c9a67-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a67-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9a67-120">-InputObject</span></span>
<span data-ttu-id="c9a67-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9a67-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c9a67-122">-Name</span></span>
<span data-ttu-id="c9a67-123">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9a67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a67-124">-ResourceGroupName</span></span>
<span data-ttu-id="c9a67-125">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9a67-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9a67-126">-SubscriptionId</span></span>
<span data-ttu-id="c9a67-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c9a67-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c9a67-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a67-129">CommonParameters</span></span>
<span data-ttu-id="c9a67-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a67-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9a67-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a67-132">입력</span><span class="sxs-lookup"><span data-stu-id="c9a67-132">INPUTS</span></span>

### <span data-ttu-id="c9a67-133">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="c9a67-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c9a67-134">출력</span><span class="sxs-lookup"><span data-stu-id="c9a67-134">OUTPUTS</span></span>

### <span data-ttu-id="c9a67-135">Microsoft. Api20200614 데이터베이스에 대 한 자세한 모든.</span><span class="sxs-lookup"><span data-stu-id="c9a67-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="c9a67-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c9a67-136">NOTES</span></span>

<span data-ttu-id="c9a67-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="c9a67-137">ALIASES</span></span>

<span data-ttu-id="c9a67-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c9a67-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9a67-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9a67-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9a67-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9a67-141">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c9a67-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9a67-142">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c9a67-143">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c9a67-144">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c9a67-145">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c9a67-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c9a67-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9a67-147">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="c9a67-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c9a67-148">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c9a67-149">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c9a67-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c9a67-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a67-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c9a67-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9a67-152">RELATED LINKS</span></span>

