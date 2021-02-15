---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184905"
---
# <span data-ttu-id="29dc6-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="29dc6-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="29dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="29dc6-103">솔루션의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="29dc6-104">구문</span><span class="sxs-lookup"><span data-stu-id="29dc6-104">SYNTAX</span></span>

### <span data-ttu-id="29dc6-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="29dc6-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29dc6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="29dc6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29dc6-107">설명</span><span class="sxs-lookup"><span data-stu-id="29dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="29dc6-108">솔루션의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="29dc6-109">예제</span><span class="sxs-lookup"><span data-stu-id="29dc6-109">EXAMPLES</span></span>

### <span data-ttu-id="29dc6-110">예제 1: 이름으로 모니터 로그 분석 솔루션 업데이트</span><span class="sxs-lookup"><span data-stu-id="29dc6-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="29dc6-111">이 명령은 이름으로 모니터 로그 분석 솔루션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="29dc6-112">예제 2: 개체에 따라 모니터 로그 분석 솔루션 업데이트</span><span class="sxs-lookup"><span data-stu-id="29dc6-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="29dc6-113">이 명령은 개체에 따라 모니터 로그 분석 솔루션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="29dc6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29dc6-114">PARAMETERS</span></span>

### <span data-ttu-id="29dc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dc6-115">-DefaultProfile</span></span>
<span data-ttu-id="29dc6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29dc6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29dc6-117">-InputObject</span></span>
<span data-ttu-id="29dc6-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="29dc6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="29dc6-119">-Name</span></span>
<span data-ttu-id="29dc6-120">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dc6-121">-ResourceGroupName</span></span>
<span data-ttu-id="29dc6-122">얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-122">The name of the resource group to get.</span></span>
<span data-ttu-id="29dc6-123">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29dc6-124">-SubscriptionId</span></span>
<span data-ttu-id="29dc6-125">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="29dc6-126">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="29dc6-127">-Tag</span></span>
<span data-ttu-id="29dc6-128">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="29dc6-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29dc6-129">-Confirm</span></span>
<span data-ttu-id="29dc6-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dc6-131">-WhatIf</span></span>
<span data-ttu-id="29dc6-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="29dc6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dc6-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dc6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dc6-134">CommonParameters</span></span>
<span data-ttu-id="29dc6-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dc6-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29dc6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dc6-137">입력</span><span class="sxs-lookup"><span data-stu-id="29dc6-137">INPUTS</span></span>

### <span data-ttu-id="29dc6-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="29dc6-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="29dc6-139">출력</span><span class="sxs-lookup"><span data-stu-id="29dc6-139">OUTPUTS</span></span>

### <span data-ttu-id="29dc6-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="29dc6-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="29dc6-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29dc6-141">NOTES</span></span>

<span data-ttu-id="29dc6-142">별칭</span><span class="sxs-lookup"><span data-stu-id="29dc6-142">ALIASES</span></span>

<span data-ttu-id="29dc6-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="29dc6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29dc6-144">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29dc6-145">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29dc6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29dc6-146">INPUTOBJECT: <IMonitoringSolutionsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="29dc6-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29dc6-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="29dc6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29dc6-148">`[ManagementAssociationName <String>]`: 사용자 ManagementAssociation 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="29dc6-149">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="29dc6-150">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="29dc6-151">`[ResourceGroupName <String>]`: 얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="29dc6-152">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="29dc6-153">`[ResourceName <String>]`: 부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="29dc6-154">`[ResourceType <String>]`: 부모 리소스의 리소스 종류</span><span class="sxs-lookup"><span data-stu-id="29dc6-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="29dc6-155">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="29dc6-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="29dc6-157">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="29dc6-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="29dc6-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29dc6-158">RELATED LINKS</span></span>

