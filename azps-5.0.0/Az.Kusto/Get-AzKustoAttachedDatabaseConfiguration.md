---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219025"
---
# <span data-ttu-id="14f3d-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="14f3d-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="14f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="14f3d-103">연결 된 데이터베이스 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="14f3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14f3d-104">SYNTAX</span></span>

### <span data-ttu-id="14f3d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="14f3d-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14f3d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="14f3d-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14f3d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14f3d-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="14f3d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="14f3d-108">DESCRIPTION</span></span>
<span data-ttu-id="14f3d-109">연결 된 데이터베이스 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="14f3d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="14f3d-110">EXAMPLES</span></span>

### <span data-ttu-id="14f3d-111">예제 1: 클러스터의 모든 AttachedDatabaseConfigurations 나열</span><span class="sxs-lookup"><span data-stu-id="14f3d-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="14f3d-112">위 명령에는 "testnewkustoclusterf" 클러스터의 모든 AttachedDatabaseConfigurations 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="14f3d-113">예제 2: 클러스터에서 특정 AttachedDatabaseConfiguration 가져오기</span><span class="sxs-lookup"><span data-stu-id="14f3d-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="14f3d-114">위 명령으로 "testnewkustoclusterf" 클러스터에 "myAttachedDatabaseConfigurations erconfiguration" 라는 이름을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="14f3d-115">변수</span><span class="sxs-lookup"><span data-stu-id="14f3d-115">PARAMETERS</span></span>

### <span data-ttu-id="14f3d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="14f3d-116">-ClusterName</span></span>
<span data-ttu-id="14f3d-117">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="14f3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f3d-118">-DefaultProfile</span></span>
<span data-ttu-id="14f3d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f3d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14f3d-120">-InputObject</span></span>
<span data-ttu-id="14f3d-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14f3d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="14f3d-122">-Name</span></span>
<span data-ttu-id="14f3d-123">연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="14f3d-125">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="14f3d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14f3d-126">-SubscriptionId</span></span>
<span data-ttu-id="14f3d-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="14f3d-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="14f3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f3d-129">CommonParameters</span></span>
<span data-ttu-id="14f3d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f3d-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14f3d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f3d-132">입력</span><span class="sxs-lookup"><span data-stu-id="14f3d-132">INPUTS</span></span>

### <span data-ttu-id="14f3d-133">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="14f3d-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="14f3d-134">출력</span><span class="sxs-lookup"><span data-stu-id="14f3d-134">OUTPUTS</span></span>

### <span data-ttu-id="14f3d-135">Microsoft. Api20200614. IAttachedDatabaseConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="14f3d-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="14f3d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="14f3d-136">NOTES</span></span>

<span data-ttu-id="14f3d-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="14f3d-137">ALIASES</span></span>

<span data-ttu-id="14f3d-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="14f3d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14f3d-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14f3d-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="14f3d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14f3d-141">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="14f3d-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14f3d-142">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="14f3d-143">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="14f3d-144">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="14f3d-145">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="14f3d-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="14f3d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14f3d-147">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="14f3d-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="14f3d-148">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="14f3d-149">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="14f3d-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="14f3d-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="14f3d-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="14f3d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14f3d-152">RELATED LINKS</span></span>

