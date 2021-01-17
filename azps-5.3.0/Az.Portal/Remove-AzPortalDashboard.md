---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491721"
---
# <span data-ttu-id="4bea9-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="4bea9-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="4bea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bea9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bea9-103">대시보드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="4bea9-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bea9-104">SYNTAX</span></span>

### <span data-ttu-id="4bea9-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="4bea9-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4bea9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4bea9-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bea9-107">설명</span><span class="sxs-lookup"><span data-stu-id="4bea9-107">DESCRIPTION</span></span>
<span data-ttu-id="4bea9-108">대시보드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="4bea9-109">예제</span><span class="sxs-lookup"><span data-stu-id="4bea9-109">EXAMPLES</span></span>

### <span data-ttu-id="4bea9-110">예제 1: 대시보드 제거</span><span class="sxs-lookup"><span data-stu-id="4bea9-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="4bea9-111">리소스 그룹 이름 및 대시보드 이름을 사용하여 Dashbaord를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="4bea9-112">예제 2: 파이프라인을 사용하여 대시보드 제거</span><span class="sxs-lookup"><span data-stu-id="4bea9-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="4bea9-113">호출에서 반환된 대시보드를 Get-AzDashboard 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="4bea9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bea9-114">PARAMETERS</span></span>

### <span data-ttu-id="4bea9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bea9-115">-DefaultProfile</span></span>
<span data-ttu-id="4bea9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bea9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bea9-117">-InputObject</span></span>
<span data-ttu-id="4bea9-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4bea9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bea9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4bea9-119">-Name</span></span>
<span data-ttu-id="4bea9-120">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bea9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bea9-121">-PassThru</span></span>
<span data-ttu-id="4bea9-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4bea9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bea9-123">-ResourceGroupName</span></span>
<span data-ttu-id="4bea9-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bea9-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bea9-125">-SubscriptionId</span></span>
<span data-ttu-id="4bea9-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-126">The Azure subscription ID.</span></span>
<span data-ttu-id="4bea9-127">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="4bea9-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4bea9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bea9-128">-Confirm</span></span>
<span data-ttu-id="4bea9-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bea9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bea9-130">-WhatIf</span></span>
<span data-ttu-id="4bea9-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4bea9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bea9-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bea9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bea9-133">CommonParameters</span></span>
<span data-ttu-id="4bea9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bea9-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4bea9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bea9-136">입력</span><span class="sxs-lookup"><span data-stu-id="4bea9-136">INPUTS</span></span>

### <span data-ttu-id="4bea9-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="4bea9-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="4bea9-138">출력</span><span class="sxs-lookup"><span data-stu-id="4bea9-138">OUTPUTS</span></span>

### <span data-ttu-id="4bea9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4bea9-139">System.Boolean</span></span>

## <span data-ttu-id="4bea9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bea9-140">NOTES</span></span>

<span data-ttu-id="4bea9-141">별칭</span><span class="sxs-lookup"><span data-stu-id="4bea9-141">ALIASES</span></span>

<span data-ttu-id="4bea9-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4bea9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bea9-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bea9-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4bea9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bea9-145">INPUTOBJECT: <IPortalIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4bea9-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bea9-146">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="4bea9-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4bea9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bea9-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4bea9-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bea9-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4bea9-150">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="4bea9-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4bea9-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bea9-151">RELATED LINKS</span></span>

