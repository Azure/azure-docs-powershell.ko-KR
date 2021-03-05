---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f3a41317663c5b1009a45bfe711cdf3410a784c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984494"
---
# <span data-ttu-id="7ccec-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="7ccec-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="7ccec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ccec-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccec-103">구독에서 솔루션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="7ccec-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ccec-104">SYNTAX</span></span>

### <span data-ttu-id="7ccec-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="7ccec-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ccec-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ccec-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ccec-107">설명</span><span class="sxs-lookup"><span data-stu-id="7ccec-107">DESCRIPTION</span></span>
<span data-ttu-id="7ccec-108">구독에서 솔루션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="7ccec-109">예제</span><span class="sxs-lookup"><span data-stu-id="7ccec-109">EXAMPLES</span></span>

### <span data-ttu-id="7ccec-110">예제 1: 이름에 의해 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="7ccec-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="7ccec-111">이 명령은 이름으로 모니터 로그 분석 솔루션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="7ccec-112">예제 2: 개체에 따라 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="7ccec-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="7ccec-113">이 명령은 개체에 따라 모니터 로그 분석 솔루션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="7ccec-114">예제 3: 파이프라인에 의해 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="7ccec-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="7ccec-115">이 명령은 파이프라인에 의해 모니터 로그 분석 솔루션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="7ccec-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ccec-116">PARAMETERS</span></span>

### <span data-ttu-id="7ccec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccec-117">-DefaultProfile</span></span>
<span data-ttu-id="7ccec-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ccec-119">-InputObject</span></span>
<span data-ttu-id="7ccec-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7ccec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ccec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7ccec-121">-Name</span></span>
<span data-ttu-id="7ccec-122">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ccec-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ccec-123">-PassThru</span></span>
<span data-ttu-id="7ccec-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ccec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ccec-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ccec-126">얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-126">The name of the resource group to get.</span></span>
<span data-ttu-id="7ccec-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ccec-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ccec-128">-SubscriptionId</span></span>
<span data-ttu-id="7ccec-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7ccec-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ccec-131">-확인</span><span class="sxs-lookup"><span data-stu-id="7ccec-131">-Confirm</span></span>
<span data-ttu-id="7ccec-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ccec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ccec-133">-WhatIf</span></span>
<span data-ttu-id="7ccec-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ccec-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ccec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccec-136">CommonParameters</span></span>
<span data-ttu-id="7ccec-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccec-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ccec-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccec-139">입력</span><span class="sxs-lookup"><span data-stu-id="7ccec-139">INPUTS</span></span>

### <span data-ttu-id="7ccec-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="7ccec-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="7ccec-141">출력</span><span class="sxs-lookup"><span data-stu-id="7ccec-141">OUTPUTS</span></span>

### <span data-ttu-id="7ccec-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7ccec-142">System.Boolean</span></span>

## <span data-ttu-id="7ccec-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ccec-143">NOTES</span></span>

<span data-ttu-id="7ccec-144">별칭</span><span class="sxs-lookup"><span data-stu-id="7ccec-144">ALIASES</span></span>

<span data-ttu-id="7ccec-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7ccec-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ccec-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ccec-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ccec-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ccec-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ccec-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ccec-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7ccec-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ccec-150">`[ManagementAssociationName <String>]`: 사용자 관리Association 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="7ccec-151">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="7ccec-152">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="7ccec-153">`[ResourceGroupName <String>]`: 얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="7ccec-154">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="7ccec-155">`[ResourceName <String>]`: 상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="7ccec-156">`[ResourceType <String>]`: 상위 리소스에 대한 리소스 유형</span><span class="sxs-lookup"><span data-stu-id="7ccec-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="7ccec-157">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="7ccec-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7ccec-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7ccec-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7ccec-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ccec-160">RELATED LINKS</span></span>

