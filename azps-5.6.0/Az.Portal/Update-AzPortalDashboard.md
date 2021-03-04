---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 97d5519d1b643a04fb1f6375030f178f9ccfbfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988946"
---
# <span data-ttu-id="4ac75-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="4ac75-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="4ac75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac75-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac75-103">기존 대시보드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="4ac75-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ac75-104">SYNTAX</span></span>

### <span data-ttu-id="4ac75-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="4ac75-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ac75-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4ac75-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ac75-107">설명</span><span class="sxs-lookup"><span data-stu-id="4ac75-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac75-108">기존 대시보드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="4ac75-109">예제</span><span class="sxs-lookup"><span data-stu-id="4ac75-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac75-110">예제 1: 대시보드의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="4ac75-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="4ac75-111">대시보드에서 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="4ac75-112">태그는 인라인 해시테이블로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="4ac75-113">예제 2: 파이프라인을 사용하여 대시보드 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="4ac75-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="4ac75-114">Get-AzPortalDashboard를 사용하여 다시 검색된 대시보드의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="4ac75-115">단일 대시보드 또는 여러 대시보드를 통해 태그를 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="4ac75-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ac75-116">PARAMETERS</span></span>

### <span data-ttu-id="4ac75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac75-117">-DefaultProfile</span></span>
<span data-ttu-id="4ac75-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac75-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ac75-119">-InputObject</span></span>
<span data-ttu-id="4ac75-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4ac75-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac75-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="4ac75-121">-Lens</span></span>
<span data-ttu-id="4ac75-122">대시보드 렌즈입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="4ac75-123">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="4ac75-123">-Metadata</span></span>
<span data-ttu-id="4ac75-124">대시보드 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="4ac75-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4ac75-125">-Name</span></span>
<span data-ttu-id="4ac75-126">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac75-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ac75-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ac75-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ac75-129">-SubscriptionId</span></span>
<span data-ttu-id="4ac75-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-130">The Azure subscription ID.</span></span>
<span data-ttu-id="4ac75-131">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4ac75-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ac75-132">-Tag</span></span>
<span data-ttu-id="4ac75-133">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="4ac75-133">Resource tags</span></span>

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

### <span data-ttu-id="4ac75-134">-확인</span><span class="sxs-lookup"><span data-stu-id="4ac75-134">-Confirm</span></span>
<span data-ttu-id="4ac75-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac75-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac75-136">-WhatIf</span></span>
<span data-ttu-id="4ac75-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac75-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac75-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac75-139">CommonParameters</span></span>
<span data-ttu-id="4ac75-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac75-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ac75-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac75-142">입력</span><span class="sxs-lookup"><span data-stu-id="4ac75-142">INPUTS</span></span>

### <span data-ttu-id="4ac75-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="4ac75-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="4ac75-144">출력</span><span class="sxs-lookup"><span data-stu-id="4ac75-144">OUTPUTS</span></span>

### <span data-ttu-id="4ac75-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="4ac75-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="4ac75-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ac75-146">NOTES</span></span>

<span data-ttu-id="4ac75-147">별칭</span><span class="sxs-lookup"><span data-stu-id="4ac75-147">ALIASES</span></span>

<span data-ttu-id="4ac75-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4ac75-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ac75-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ac75-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ac75-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ac75-151">INPUTOBJECT <IPortalIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ac75-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ac75-152">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="4ac75-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4ac75-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ac75-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4ac75-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4ac75-156">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="4ac75-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4ac75-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ac75-157">RELATED LINKS</span></span>

