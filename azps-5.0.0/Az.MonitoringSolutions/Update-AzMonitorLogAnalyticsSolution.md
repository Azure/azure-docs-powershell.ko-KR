---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226118"
---
# <span data-ttu-id="8bf1a-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="8bf1a-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="8bf1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf1a-103">솔루션의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="8bf1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8bf1a-104">SYNTAX</span></span>

### <span data-ttu-id="8bf1a-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8bf1a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8bf1a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8bf1a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8bf1a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8bf1a-107">DESCRIPTION</span></span>
<span data-ttu-id="8bf1a-108">솔루션의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="8bf1a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8bf1a-109">EXAMPLES</span></span>

### <span data-ttu-id="8bf1a-110">예제 1: 이름별로 모니터 로그 분석 솔루션 업데이트</span><span class="sxs-lookup"><span data-stu-id="8bf1a-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="8bf1a-111">이 명령은 모니터 로그 분석 솔루션을 이름으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="8bf1a-112">예제 2: 개체 별로 모니터 로그 분석 솔루션 업데이트</span><span class="sxs-lookup"><span data-stu-id="8bf1a-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="8bf1a-113">이 명령은 모니터 로그 분석 솔루션을 개체 별로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="8bf1a-114">변수</span><span class="sxs-lookup"><span data-stu-id="8bf1a-114">PARAMETERS</span></span>

### <span data-ttu-id="8bf1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf1a-115">-DefaultProfile</span></span>
<span data-ttu-id="8bf1a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf1a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bf1a-117">-InputObject</span></span>
<span data-ttu-id="8bf1a-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bf1a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8bf1a-119">-Name</span></span>
<span data-ttu-id="8bf1a-120">사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-120">User Solution Name.</span></span>

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

### <span data-ttu-id="8bf1a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf1a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8bf1a-122">가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-122">The name of the resource group to get.</span></span>
<span data-ttu-id="8bf1a-123">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8bf1a-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bf1a-124">-SubscriptionId</span></span>
<span data-ttu-id="8bf1a-125">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8bf1a-126">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8bf1a-127">태그</span><span class="sxs-lookup"><span data-stu-id="8bf1a-127">-Tag</span></span>
<span data-ttu-id="8bf1a-128">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="8bf1a-128">Resource tags</span></span>

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

### <span data-ttu-id="8bf1a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="8bf1a-129">-Confirm</span></span>
<span data-ttu-id="8bf1a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf1a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf1a-131">-WhatIf</span></span>
<span data-ttu-id="8bf1a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf1a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf1a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf1a-134">CommonParameters</span></span>
<span data-ttu-id="8bf1a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf1a-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf1a-137">입력</span><span class="sxs-lookup"><span data-stu-id="8bf1a-137">INPUTS</span></span>

### <span data-ttu-id="8bf1a-138">MonitoringSolutions. IMonitoringSolutionsIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="8bf1a-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="8bf1a-139">출력</span><span class="sxs-lookup"><span data-stu-id="8bf1a-139">OUTPUTS</span></span>

### <span data-ttu-id="8bf1a-140">MonitoringSolutions. Api20151101Preview. ISolution에 대 한</span><span class="sxs-lookup"><span data-stu-id="8bf1a-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="8bf1a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8bf1a-141">NOTES</span></span>

<span data-ttu-id="8bf1a-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="8bf1a-142">ALIASES</span></span>

<span data-ttu-id="8bf1a-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8bf1a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8bf1a-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bf1a-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8bf1a-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8bf1a-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8bf1a-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8bf1a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8bf1a-148">`[ManagementAssociationName <String>]`: 사용자 ManagementAssociation 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="8bf1a-149">`[ManagementConfigurationName <String>]`: 사용자 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="8bf1a-150">`[ProviderName <String>]`: 부모 리소스의 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="8bf1a-151">`[ResourceGroupName <String>]`: 가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="8bf1a-152">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="8bf1a-153">`[ResourceName <String>]`: 부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="8bf1a-154">`[ResourceType <String>]`: 상위 자원의 자원 종류</span><span class="sxs-lookup"><span data-stu-id="8bf1a-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="8bf1a-155">`[SolutionName <String>]`: 사용자 솔루션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="8bf1a-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8bf1a-157">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf1a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8bf1a-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bf1a-158">RELATED LINKS</span></span>

