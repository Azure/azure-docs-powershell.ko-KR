---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214272"
---
# <span data-ttu-id="7ea3d-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="7ea3d-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="7ea3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea3d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea3d-103">기존 대시보드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="7ea3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ea3d-104">SYNTAX</span></span>

### <span data-ttu-id="7ea3d-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ea3d-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ea3d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7ea3d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ea3d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ea3d-107">DESCRIPTION</span></span>
<span data-ttu-id="7ea3d-108">기존 대시보드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="7ea3d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7ea3d-109">EXAMPLES</span></span>

### <span data-ttu-id="7ea3d-110">예제 1: 대시보드의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea3d-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="7ea3d-111">대시보드의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="7ea3d-112">태그는 인라인 hashtable로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="7ea3d-113">예제 2: 파이프라인을 사용 하 여 대시보드 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea3d-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="7ea3d-114">AzPortalDashboard를 사용 하 여 다시 시도 된 대시보드의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="7ea3d-115">이를 사용 하 여 단일 대시보드 또는 여러 일점 dashboard fs를 통해 태그를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="7ea3d-116">변수</span><span class="sxs-lookup"><span data-stu-id="7ea3d-116">PARAMETERS</span></span>

### <span data-ttu-id="7ea3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea3d-117">-DefaultProfile</span></span>
<span data-ttu-id="7ea3d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ea3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ea3d-119">-InputObject</span></span>
<span data-ttu-id="7ea3d-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ea3d-121">-렌즈</span><span class="sxs-lookup"><span data-stu-id="7ea3d-121">-Lens</span></span>
<span data-ttu-id="7ea3d-122">대시보드 렌즈.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="7ea3d-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7ea3d-123">-Metadata</span></span>
<span data-ttu-id="7ea3d-124">대시보드 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="7ea3d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="7ea3d-125">-Name</span></span>
<span data-ttu-id="7ea3d-126">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="7ea3d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea3d-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ea3d-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ea3d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ea3d-129">-SubscriptionId</span></span>
<span data-ttu-id="7ea3d-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-130">The Azure subscription ID.</span></span>
<span data-ttu-id="7ea3d-131">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7ea3d-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7ea3d-132">태그</span><span class="sxs-lookup"><span data-stu-id="7ea3d-132">-Tag</span></span>
<span data-ttu-id="7ea3d-133">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="7ea3d-133">Resource tags</span></span>

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

### <span data-ttu-id="7ea3d-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7ea3d-134">-Confirm</span></span>
<span data-ttu-id="7ea3d-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea3d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea3d-136">-WhatIf</span></span>
<span data-ttu-id="7ea3d-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea3d-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea3d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea3d-139">CommonParameters</span></span>
<span data-ttu-id="7ea3d-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea3d-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea3d-142">입력</span><span class="sxs-lookup"><span data-stu-id="7ea3d-142">INPUTS</span></span>

### <span data-ttu-id="7ea3d-143">IPortalIdentity (Microsoft. PowerShell. 포털)</span><span class="sxs-lookup"><span data-stu-id="7ea3d-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="7ea3d-144">출력</span><span class="sxs-lookup"><span data-stu-id="7ea3d-144">OUTPUTS</span></span>

### <span data-ttu-id="7ea3d-145">Api201901Preview. i i m. i m a. i m a. i a Idashboard</span><span class="sxs-lookup"><span data-stu-id="7ea3d-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="7ea3d-146">상속자</span><span class="sxs-lookup"><span data-stu-id="7ea3d-146">NOTES</span></span>

<span data-ttu-id="7ea3d-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="7ea3d-147">ALIASES</span></span>

<span data-ttu-id="7ea3d-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7ea3d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ea3d-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ea3d-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ea3d-151">INPUTOBJECT <IPortalIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ea3d-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ea3d-152">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="7ea3d-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="7ea3d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ea3d-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7ea3d-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea3d-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7ea3d-156">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7ea3d-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7ea3d-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ea3d-157">RELATED LINKS</span></span>

