---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361593"
---
# <span data-ttu-id="4aaa6-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4aaa6-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="4aaa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaa6-103">연결된 데이터베이스 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="4aaa6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4aaa6-104">SYNTAX</span></span>

### <span data-ttu-id="4aaa6-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="4aaa6-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4aaa6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4aaa6-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4aaa6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4aaa6-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4aaa6-108">설명</span><span class="sxs-lookup"><span data-stu-id="4aaa6-108">DESCRIPTION</span></span>
<span data-ttu-id="4aaa6-109">연결된 데이터베이스 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="4aaa6-110">예제</span><span class="sxs-lookup"><span data-stu-id="4aaa6-110">EXAMPLES</span></span>

### <span data-ttu-id="4aaa6-111">예제 1: 클러스터의 모든 AttachedDatabaseConfigurations 나열</span><span class="sxs-lookup"><span data-stu-id="4aaa6-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="4aaa6-112">위의 명령은 "testnewkustoclusterf" 클러스터의 모든 AttachedDatabaseConfigurations를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="4aaa6-113">예제 2: 클러스터에서 특정 AttachedDatabaseConfiguration을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="4aaa6-114">위의 명령은 "testnewkustoclusterf" 클러스터에 "myfollowerconfiguration"이라는 AttachedDatabaseConfigurations를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="4aaa6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aaa6-115">PARAMETERS</span></span>

### <span data-ttu-id="4aaa6-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4aaa6-116">-ClusterName</span></span>
<span data-ttu-id="4aaa6-117">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4aaa6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaa6-118">-DefaultProfile</span></span>
<span data-ttu-id="4aaa6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aaa6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aaa6-120">-InputObject</span></span>
<span data-ttu-id="4aaa6-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4aaa6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4aaa6-122">-Name</span></span>
<span data-ttu-id="4aaa6-123">연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-123">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="4aaa6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aaa6-124">-ResourceGroupName</span></span>
<span data-ttu-id="4aaa6-125">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4aaa6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4aaa6-126">-SubscriptionId</span></span>
<span data-ttu-id="4aaa6-127">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4aaa6-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4aaa6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaa6-129">CommonParameters</span></span>
<span data-ttu-id="4aaa6-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaa6-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaa6-132">입력</span><span class="sxs-lookup"><span data-stu-id="4aaa6-132">INPUTS</span></span>

### <span data-ttu-id="4aaa6-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4aaa6-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4aaa6-134">출력</span><span class="sxs-lookup"><span data-stu-id="4aaa6-134">OUTPUTS</span></span>

### <span data-ttu-id="4aaa6-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4aaa6-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="4aaa6-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4aaa6-136">NOTES</span></span>

<span data-ttu-id="4aaa6-137">별칭</span><span class="sxs-lookup"><span data-stu-id="4aaa6-137">ALIASES</span></span>

<span data-ttu-id="4aaa6-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4aaa6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4aaa6-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4aaa6-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4aaa6-141">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4aaa6-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4aaa6-142">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4aaa6-143">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4aaa6-144">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4aaa6-145">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4aaa6-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4aaa6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4aaa6-147">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4aaa6-148">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4aaa6-149">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4aaa6-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4aaa6-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaa6-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4aaa6-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aaa6-152">RELATED LINKS</span></span>

