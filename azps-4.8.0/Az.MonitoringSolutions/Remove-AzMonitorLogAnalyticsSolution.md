---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048979"
---
# <span data-ttu-id="8d093-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="8d093-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="8d093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d093-102">SYNOPSIS</span></span>
<span data-ttu-id="8d093-103">구독에서 솔루션을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="8d093-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d093-104">SYNTAX</span></span>

### <span data-ttu-id="8d093-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d093-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d093-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d093-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d093-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d093-107">DESCRIPTION</span></span>
<span data-ttu-id="8d093-108">구독에서 솔루션을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="8d093-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8d093-109">EXAMPLES</span></span>

### <span data-ttu-id="8d093-110">예제 1: 이름별로 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="8d093-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="8d093-111">이 명령은 모니터 로그 분석 솔루션을 이름으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="8d093-112">예제 2: 개체 별로 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="8d093-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="8d093-113">이 명령은 모니터 로그 분석 솔루션을 개체 별로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="8d093-114">예제 3: 파이프라인에 따라 모니터 로그 분석 솔루션 제거</span><span class="sxs-lookup"><span data-stu-id="8d093-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="8d093-115">이 명령은 파이프라인 별로 모니터 로그 분석 솔루션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="8d093-116">변수</span><span class="sxs-lookup"><span data-stu-id="8d093-116">PARAMETERS</span></span>

### <span data-ttu-id="8d093-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d093-117">-DefaultProfile</span></span>
<span data-ttu-id="8d093-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d093-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d093-119">-InputObject</span></span>
<span data-ttu-id="8d093-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d093-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8d093-121">-Name</span></span>
<span data-ttu-id="8d093-122">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-122">User Solution Name.</span></span>

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

### <span data-ttu-id="8d093-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d093-123">-PassThru</span></span>
<span data-ttu-id="8d093-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8d093-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d093-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d093-126">가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-126">The name of the resource group to get.</span></span>
<span data-ttu-id="8d093-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d093-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d093-128">-SubscriptionId</span></span>
<span data-ttu-id="8d093-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d093-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d093-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8d093-131">-Confirm</span></span>
<span data-ttu-id="8d093-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d093-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d093-133">-WhatIf</span></span>
<span data-ttu-id="8d093-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d093-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d093-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d093-136">CommonParameters</span></span>
<span data-ttu-id="8d093-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d093-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d093-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d093-139">입력</span><span class="sxs-lookup"><span data-stu-id="8d093-139">INPUTS</span></span>

### <span data-ttu-id="8d093-140">MonitoringSolutions. IMonitoringSolutionsIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d093-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="8d093-141">출력</span><span class="sxs-lookup"><span data-stu-id="8d093-141">OUTPUTS</span></span>

### <span data-ttu-id="8d093-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8d093-142">System.Boolean</span></span>

## <span data-ttu-id="8d093-143">상속자</span><span class="sxs-lookup"><span data-stu-id="8d093-143">NOTES</span></span>

<span data-ttu-id="8d093-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="8d093-144">ALIASES</span></span>

<span data-ttu-id="8d093-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8d093-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d093-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d093-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d093-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d093-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8d093-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d093-149">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8d093-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d093-150">`[ManagementAssociationName <String>]`: 사용자 ManagementAssociation 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="8d093-151">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="8d093-152">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="8d093-153">`[ResourceGroupName <String>]`: 가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="8d093-154">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d093-155">`[ResourceName <String>]`: 부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="8d093-156">`[ResourceType <String>]`: 상위 자원의 자원 종류</span><span class="sxs-lookup"><span data-stu-id="8d093-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="8d093-157">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="8d093-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8d093-159">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d093-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8d093-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d093-160">RELATED LINKS</span></span>

