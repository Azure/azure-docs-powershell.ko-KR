---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187337"
---
# <span data-ttu-id="db818-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="db818-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="db818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db818-102">SYNOPSIS</span></span>
<span data-ttu-id="db818-103">구독에서 솔루션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="db818-104">구문</span><span class="sxs-lookup"><span data-stu-id="db818-104">SYNTAX</span></span>

### <span data-ttu-id="db818-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="db818-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db818-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db818-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db818-107">설명</span><span class="sxs-lookup"><span data-stu-id="db818-107">DESCRIPTION</span></span>
<span data-ttu-id="db818-108">구독에서 솔루션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="db818-109">예제</span><span class="sxs-lookup"><span data-stu-id="db818-109">EXAMPLES</span></span>

### <span data-ttu-id="db818-110">예제 1: 이름으로 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="db818-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="db818-111">이 명령은 이름으로 모니터 로그 분석 솔루션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="db818-112">예제 2: 개체에 따라 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="db818-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="db818-113">이 명령은 개체에 따라 모니터 로그 분석 솔루션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="db818-114">예제 3: 파이프라인에 의해 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="db818-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="db818-115">이 명령은 파이프라인에 의해 모니터 로그 분석 솔루션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="db818-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db818-116">PARAMETERS</span></span>

### <span data-ttu-id="db818-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db818-117">-DefaultProfile</span></span>
<span data-ttu-id="db818-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db818-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db818-119">-InputObject</span></span>
<span data-ttu-id="db818-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="db818-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db818-121">-Name</span><span class="sxs-lookup"><span data-stu-id="db818-121">-Name</span></span>
<span data-ttu-id="db818-122">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-122">User Solution Name.</span></span>

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

### <span data-ttu-id="db818-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db818-123">-PassThru</span></span>
<span data-ttu-id="db818-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="db818-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db818-125">-ResourceGroupName</span></span>
<span data-ttu-id="db818-126">얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-126">The name of the resource group to get.</span></span>
<span data-ttu-id="db818-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="db818-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db818-128">-SubscriptionId</span></span>
<span data-ttu-id="db818-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db818-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db818-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db818-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db818-131">-Confirm</span></span>
<span data-ttu-id="db818-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db818-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db818-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db818-133">-WhatIf</span></span>
<span data-ttu-id="db818-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="db818-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db818-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db818-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db818-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db818-136">CommonParameters</span></span>
<span data-ttu-id="db818-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db818-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db818-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db818-139">입력</span><span class="sxs-lookup"><span data-stu-id="db818-139">INPUTS</span></span>

### <span data-ttu-id="db818-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="db818-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="db818-141">출력</span><span class="sxs-lookup"><span data-stu-id="db818-141">OUTPUTS</span></span>

### <span data-ttu-id="db818-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db818-142">System.Boolean</span></span>

## <span data-ttu-id="db818-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db818-143">NOTES</span></span>

<span data-ttu-id="db818-144">별칭</span><span class="sxs-lookup"><span data-stu-id="db818-144">ALIASES</span></span>

<span data-ttu-id="db818-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="db818-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db818-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db818-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db818-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db818-148">INPUTOBJECT: <IMonitoringSolutionsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="db818-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db818-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="db818-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db818-150">`[ManagementAssociationName <String>]`: 사용자 ManagementAssociation 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="db818-151">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="db818-152">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="db818-153">`[ResourceGroupName <String>]`: 얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="db818-154">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="db818-155">`[ResourceName <String>]`: 부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="db818-156">`[ResourceType <String>]`: 부모 리소스의 리소스 종류</span><span class="sxs-lookup"><span data-stu-id="db818-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="db818-157">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db818-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="db818-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db818-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="db818-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="db818-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="db818-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db818-160">RELATED LINKS</span></span>

