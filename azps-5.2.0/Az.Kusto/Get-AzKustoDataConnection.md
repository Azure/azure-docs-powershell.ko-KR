---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349305"
---
# <span data-ttu-id="716c7-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="716c7-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="716c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="716c7-102">SYNOPSIS</span></span>
<span data-ttu-id="716c7-103">데이터 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-103">Returns a data connection.</span></span>

## <span data-ttu-id="716c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="716c7-104">SYNTAX</span></span>

### <span data-ttu-id="716c7-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="716c7-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="716c7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="716c7-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="716c7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="716c7-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="716c7-108">설명</span><span class="sxs-lookup"><span data-stu-id="716c7-108">DESCRIPTION</span></span>
<span data-ttu-id="716c7-109">데이터 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-109">Returns a data connection.</span></span>

## <span data-ttu-id="716c7-110">예제</span><span class="sxs-lookup"><span data-stu-id="716c7-110">EXAMPLES</span></span>

### <span data-ttu-id="716c7-111">예제 1: 특정 데이터베이스의 모든 데이터 연결 나열</span><span class="sxs-lookup"><span data-stu-id="716c7-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="716c7-112">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"의 모든 Kusto 데이터베이스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="716c7-113">예제 2: 이름별 특정 데이터 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="716c7-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="716c7-114">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에서 "mykustodataconnection"이라는 데이터 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="716c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="716c7-115">PARAMETERS</span></span>

### <span data-ttu-id="716c7-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="716c7-116">-ClusterName</span></span>
<span data-ttu-id="716c7-117">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="716c7-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="716c7-118">-DatabaseName</span></span>
<span data-ttu-id="716c7-119">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="716c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716c7-120">-DefaultProfile</span></span>
<span data-ttu-id="716c7-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="716c7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="716c7-122">-InputObject</span></span>
<span data-ttu-id="716c7-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="716c7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="716c7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="716c7-124">-Name</span></span>
<span data-ttu-id="716c7-125">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="716c7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716c7-126">-ResourceGroupName</span></span>
<span data-ttu-id="716c7-127">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="716c7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="716c7-128">-SubscriptionId</span></span>
<span data-ttu-id="716c7-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="716c7-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="716c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716c7-131">CommonParameters</span></span>
<span data-ttu-id="716c7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716c7-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="716c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716c7-134">입력</span><span class="sxs-lookup"><span data-stu-id="716c7-134">INPUTS</span></span>

### <span data-ttu-id="716c7-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="716c7-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="716c7-136">출력</span><span class="sxs-lookup"><span data-stu-id="716c7-136">OUTPUTS</span></span>

### <span data-ttu-id="716c7-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="716c7-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="716c7-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="716c7-138">NOTES</span></span>

<span data-ttu-id="716c7-139">별칭</span><span class="sxs-lookup"><span data-stu-id="716c7-139">ALIASES</span></span>

<span data-ttu-id="716c7-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="716c7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="716c7-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="716c7-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="716c7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="716c7-143">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="716c7-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="716c7-144">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="716c7-145">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="716c7-146">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="716c7-147">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="716c7-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="716c7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="716c7-149">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="716c7-150">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="716c7-151">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="716c7-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="716c7-153">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="716c7-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="716c7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="716c7-154">RELATED LINKS</span></span>

