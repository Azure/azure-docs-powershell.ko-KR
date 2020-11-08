---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226741"
---
# <span data-ttu-id="3280b-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="3280b-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="3280b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3280b-102">SYNOPSIS</span></span>
<span data-ttu-id="3280b-103">사용자 솔루션을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="3280b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3280b-104">SYNTAX</span></span>

### <span data-ttu-id="3280b-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3280b-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3280b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="3280b-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3280b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3280b-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3280b-108">목록</span><span class="sxs-lookup"><span data-stu-id="3280b-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3280b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3280b-109">DESCRIPTION</span></span>
<span data-ttu-id="3280b-110">사용자 솔루션을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="3280b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3280b-111">EXAMPLES</span></span>

### <span data-ttu-id="3280b-112">예제 1: 이름별로 모니터 로그 분석 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="3280b-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="3280b-113">이 명령은 이름으로 모니터 로그 분석 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="3280b-114">예제 2: 리소스 id 별 모니터 로그 분석 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="3280b-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="3280b-115">이 명령은 리소스 id를 기준으로 모니터 로그 분석 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="3280b-116">예제 3: 개체 별로 모니터 로그 분석 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="3280b-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="3280b-117">이 명령은 개체 별로 모니터 로그 분석 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="3280b-118">예제 4: 리소스 그룹 아래에 모든 모니터 로그 분석 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="3280b-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="3280b-119">이 명령은 리소스 그룹 아래에 있는 모든 모니터 로그 분석 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="3280b-120">예제 5: 구독에서 모든 모니터 로그 분석 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="3280b-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="3280b-121">이 명령은 구독 하는 모든 모니터 로그 분석 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="3280b-122">변수</span><span class="sxs-lookup"><span data-stu-id="3280b-122">PARAMETERS</span></span>

### <span data-ttu-id="3280b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3280b-123">-DefaultProfile</span></span>
<span data-ttu-id="3280b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3280b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3280b-125">-InputObject</span></span>
<span data-ttu-id="3280b-126">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3280b-127">-이름</span><span class="sxs-lookup"><span data-stu-id="3280b-127">-Name</span></span>
<span data-ttu-id="3280b-128">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3280b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3280b-129">-ResourceGroupName</span></span>
<span data-ttu-id="3280b-130">가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-130">The name of the resource group to get.</span></span>
<span data-ttu-id="3280b-131">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3280b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3280b-132">-SubscriptionId</span></span>
<span data-ttu-id="3280b-133">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3280b-134">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3280b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3280b-135">CommonParameters</span></span>
<span data-ttu-id="3280b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3280b-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3280b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3280b-138">입력</span><span class="sxs-lookup"><span data-stu-id="3280b-138">INPUTS</span></span>

### <span data-ttu-id="3280b-139">MonitoringSolutions. IMonitoringSolutionsIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="3280b-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="3280b-140">출력</span><span class="sxs-lookup"><span data-stu-id="3280b-140">OUTPUTS</span></span>

### <span data-ttu-id="3280b-141">MonitoringSolutions. Api20151101Preview. ISolution에 대 한</span><span class="sxs-lookup"><span data-stu-id="3280b-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="3280b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="3280b-142">NOTES</span></span>

<span data-ttu-id="3280b-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="3280b-143">ALIASES</span></span>

<span data-ttu-id="3280b-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3280b-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3280b-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3280b-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="3280b-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3280b-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3280b-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3280b-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="3280b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3280b-149">`[ManagementAssociationName <String>]`: 사용자 ManagementAssociation 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="3280b-150">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="3280b-151">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="3280b-152">`[ResourceGroupName <String>]`: 가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="3280b-153">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="3280b-154">`[ResourceName <String>]`: 부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="3280b-155">`[ResourceType <String>]`: 상위 자원의 자원 종류</span><span class="sxs-lookup"><span data-stu-id="3280b-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="3280b-156">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="3280b-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3280b-158">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3280b-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3280b-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3280b-159">RELATED LINKS</span></span>

