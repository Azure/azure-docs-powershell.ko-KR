---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187372"
---
# <span data-ttu-id="f23ac-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="f23ac-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="f23ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f23ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f23ac-103">사용자 솔루션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="f23ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="f23ac-104">SYNTAX</span></span>

### <span data-ttu-id="f23ac-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="f23ac-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f23ac-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f23ac-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f23ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f23ac-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f23ac-108">목록</span><span class="sxs-lookup"><span data-stu-id="f23ac-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f23ac-109">설명</span><span class="sxs-lookup"><span data-stu-id="f23ac-109">DESCRIPTION</span></span>
<span data-ttu-id="f23ac-110">사용자 솔루션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="f23ac-111">예제</span><span class="sxs-lookup"><span data-stu-id="f23ac-111">EXAMPLES</span></span>

### <span data-ttu-id="f23ac-112">예제 1: 이름으로 모니터 로그 분석 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="f23ac-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f23ac-113">이 명령은 이름으로 모니터 로그 분석 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="f23ac-114">예제 2: 리소스 ID로 모니터 로그 분석 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="f23ac-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="f23ac-115">이 명령은 리소스 ID로 모니터 로그 분석 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="f23ac-116">예제 3: 개체로 모니터 로그 분석 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="f23ac-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f23ac-117">이 명령은 개체에 따라 모니터 로그 분석 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="f23ac-118">예제 4: 리소스 그룹에서 모든 모니터 로그 분석 솔루션 사용</span><span class="sxs-lookup"><span data-stu-id="f23ac-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f23ac-119">이 명령은 리소스 그룹에서 모든 모니터 로그 분석 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="f23ac-120">예제 5: 구독에서 모든 모니터 로그 분석 솔루션 사용</span><span class="sxs-lookup"><span data-stu-id="f23ac-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f23ac-121">이 명령은 구독에서 모든 모니터 로그 분석 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="f23ac-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f23ac-122">PARAMETERS</span></span>

### <span data-ttu-id="f23ac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23ac-123">-DefaultProfile</span></span>
<span data-ttu-id="f23ac-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f23ac-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f23ac-125">-InputObject</span></span>
<span data-ttu-id="f23ac-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f23ac-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f23ac-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f23ac-127">-Name</span></span>
<span data-ttu-id="f23ac-128">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-128">User Solution Name.</span></span>

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

### <span data-ttu-id="f23ac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23ac-129">-ResourceGroupName</span></span>
<span data-ttu-id="f23ac-130">얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-130">The name of the resource group to get.</span></span>
<span data-ttu-id="f23ac-131">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f23ac-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f23ac-132">-SubscriptionId</span></span>
<span data-ttu-id="f23ac-133">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f23ac-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f23ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23ac-135">CommonParameters</span></span>
<span data-ttu-id="f23ac-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23ac-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f23ac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23ac-138">입력</span><span class="sxs-lookup"><span data-stu-id="f23ac-138">INPUTS</span></span>

### <span data-ttu-id="f23ac-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="f23ac-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="f23ac-140">출력</span><span class="sxs-lookup"><span data-stu-id="f23ac-140">OUTPUTS</span></span>

### <span data-ttu-id="f23ac-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="f23ac-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="f23ac-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f23ac-142">NOTES</span></span>

<span data-ttu-id="f23ac-143">별칭</span><span class="sxs-lookup"><span data-stu-id="f23ac-143">ALIASES</span></span>

<span data-ttu-id="f23ac-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f23ac-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f23ac-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f23ac-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f23ac-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f23ac-147">INPUTOBJECT: <IMonitoringSolutionsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f23ac-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f23ac-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f23ac-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f23ac-149">`[ManagementAssociationName <String>]`: 사용자 ManagementAssociation 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="f23ac-150">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="f23ac-151">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="f23ac-152">`[ResourceGroupName <String>]`: 얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="f23ac-153">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="f23ac-154">`[ResourceName <String>]`: 부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="f23ac-155">`[ResourceType <String>]`: 부모 리소스의 리소스 종류</span><span class="sxs-lookup"><span data-stu-id="f23ac-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="f23ac-156">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="f23ac-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f23ac-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="f23ac-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f23ac-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f23ac-159">RELATED LINKS</span></span>

