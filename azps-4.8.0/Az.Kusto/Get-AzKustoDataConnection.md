---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056685"
---
# <span data-ttu-id="12917-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="12917-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="12917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12917-102">SYNOPSIS</span></span>
<span data-ttu-id="12917-103">데이터 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-103">Returns a data connection.</span></span>

## <span data-ttu-id="12917-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12917-104">SYNTAX</span></span>

### <span data-ttu-id="12917-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="12917-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12917-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="12917-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12917-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12917-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="12917-108">설명은</span><span class="sxs-lookup"><span data-stu-id="12917-108">DESCRIPTION</span></span>
<span data-ttu-id="12917-109">데이터 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-109">Returns a data connection.</span></span>

## <span data-ttu-id="12917-110">예제의</span><span class="sxs-lookup"><span data-stu-id="12917-110">EXAMPLES</span></span>

### <span data-ttu-id="12917-111">예제 1: 특정 데이터베이스의 모든 데이터 연결 목록 표시</span><span class="sxs-lookup"><span data-stu-id="12917-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12917-112">위의 명령은 리소스 그룹 "testrg"에 있는 "testnewkustocluster" 클러스터의 모든 Kusto 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="12917-113">예제 2: 이름으로 특정 데이터 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="12917-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="12917-114">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 있는 "mykustodataconnection" 데이터 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="12917-115">변수</span><span class="sxs-lookup"><span data-stu-id="12917-115">PARAMETERS</span></span>

### <span data-ttu-id="12917-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="12917-116">-ClusterName</span></span>
<span data-ttu-id="12917-117">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="12917-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12917-118">-DatabaseName</span></span>
<span data-ttu-id="12917-119">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="12917-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12917-120">-DefaultProfile</span></span>
<span data-ttu-id="12917-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12917-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12917-122">-InputObject</span></span>
<span data-ttu-id="12917-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12917-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12917-124">-이름</span><span class="sxs-lookup"><span data-stu-id="12917-124">-Name</span></span>
<span data-ttu-id="12917-125">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12917-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12917-126">-ResourceGroupName</span></span>
<span data-ttu-id="12917-127">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="12917-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12917-128">-SubscriptionId</span></span>
<span data-ttu-id="12917-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12917-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12917-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12917-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12917-131">CommonParameters</span></span>
<span data-ttu-id="12917-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12917-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12917-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12917-134">입력</span><span class="sxs-lookup"><span data-stu-id="12917-134">INPUTS</span></span>

### <span data-ttu-id="12917-135">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="12917-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="12917-136">출력</span><span class="sxs-lookup"><span data-stu-id="12917-136">OUTPUTS</span></span>

### <span data-ttu-id="12917-137">Microsoft. Api20200614. IDataConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="12917-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="12917-138">상속자</span><span class="sxs-lookup"><span data-stu-id="12917-138">NOTES</span></span>

<span data-ttu-id="12917-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="12917-139">ALIASES</span></span>

<span data-ttu-id="12917-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="12917-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12917-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12917-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="12917-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12917-143">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="12917-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12917-144">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="12917-145">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="12917-146">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="12917-147">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="12917-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="12917-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12917-149">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="12917-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="12917-150">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="12917-151">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12917-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="12917-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12917-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12917-153">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="12917-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12917-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12917-154">RELATED LINKS</span></span>

