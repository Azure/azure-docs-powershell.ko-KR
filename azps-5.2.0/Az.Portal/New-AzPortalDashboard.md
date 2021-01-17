---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370896"
---
# <span data-ttu-id="a6705-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="a6705-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="a6705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6705-102">SYNOPSIS</span></span>
<span data-ttu-id="a6705-103">대시보드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a6705-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6705-104">SYNTAX</span></span>

### <span data-ttu-id="a6705-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6705-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6705-106">만들기</span><span class="sxs-lookup"><span data-stu-id="a6705-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6705-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="a6705-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6705-108">설명</span><span class="sxs-lookup"><span data-stu-id="a6705-108">DESCRIPTION</span></span>
<span data-ttu-id="a6705-109">대시보드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a6705-110">예제</span><span class="sxs-lookup"><span data-stu-id="a6705-110">EXAMPLES</span></span>

### <span data-ttu-id="a6705-111">예제 1: 대시보드 템플릿 파일을 사용하여 대시보드 만들기</span><span class="sxs-lookup"><span data-stu-id="a6705-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="a6705-112">제공된 대시보드 템플릿 파일을 사용하여 새 대시보드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="a6705-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6705-113">PARAMETERS</span></span>

### <span data-ttu-id="a6705-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="a6705-114">-Dashboard</span></span>
<span data-ttu-id="a6705-115">공유 대시보드 리소스 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="a6705-116">구성을 위해 대시보드 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a6705-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="a6705-117">-DashboardPath</span></span>
<span data-ttu-id="a6705-118">기존 대시보드 템플릿에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="a6705-119">대시보드 템플릿은 포털에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6705-120">-DefaultProfile</span></span>
<span data-ttu-id="a6705-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6705-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="a6705-122">-Lens</span></span>
<span data-ttu-id="a6705-123">대시보드는 렌즈를 습니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-124">-Location</span><span class="sxs-lookup"><span data-stu-id="a6705-124">-Location</span></span>
<span data-ttu-id="a6705-125">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="a6705-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a6705-126">-Metadata</span></span>
<span data-ttu-id="a6705-127">대시보드 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a6705-128">-Name</span></span>
<span data-ttu-id="a6705-129">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6705-130">-ResourceGroupName</span></span>
<span data-ttu-id="a6705-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6705-132">-SubscriptionId</span></span>
<span data-ttu-id="a6705-133">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-133">The Azure subscription ID.</span></span>
<span data-ttu-id="a6705-134">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a6705-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6705-135">-Tag</span></span>
<span data-ttu-id="a6705-136">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="a6705-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6705-137">-Confirm</span></span>
<span data-ttu-id="a6705-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6705-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6705-139">-WhatIf</span></span>
<span data-ttu-id="a6705-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a6705-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6705-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6705-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6705-142">CommonParameters</span></span>
<span data-ttu-id="a6705-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6705-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6705-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6705-145">입력</span><span class="sxs-lookup"><span data-stu-id="a6705-145">INPUTS</span></span>

### <span data-ttu-id="a6705-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="a6705-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a6705-147">출력</span><span class="sxs-lookup"><span data-stu-id="a6705-147">OUTPUTS</span></span>

### <span data-ttu-id="a6705-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="a6705-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a6705-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6705-149">NOTES</span></span>

<span data-ttu-id="a6705-150">별칭</span><span class="sxs-lookup"><span data-stu-id="a6705-150">ALIASES</span></span>

<span data-ttu-id="a6705-151">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a6705-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6705-152">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6705-153">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6705-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6705-154">대시보드: <IDashboard> 공유 대시보드 리소스 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="a6705-155">`Location <String>`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="a6705-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="a6705-156">`[Lens <IDashboardPropertiesLenses>]`: 대시보드 렌즈입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="a6705-157">`[(Any) <IDashboardLens>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a6705-158">`[Metadata <IDashboardPropertiesMetadata>]`: 대시보드 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="a6705-159">`[(Any) <Object>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a6705-160">`[Tag <IDashboardTags>]`: 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="a6705-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="a6705-161">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6705-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="a6705-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6705-162">RELATED LINKS</span></span>

