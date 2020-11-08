---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214280"
---
# <span data-ttu-id="c39a1-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="c39a1-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="c39a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c39a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c39a1-103">대시보드를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="c39a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c39a1-104">SYNTAX</span></span>

### <span data-ttu-id="c39a1-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="c39a1-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c39a1-106">만드는</span><span class="sxs-lookup"><span data-stu-id="c39a1-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c39a1-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="c39a1-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c39a1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c39a1-108">DESCRIPTION</span></span>
<span data-ttu-id="c39a1-109">대시보드를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="c39a1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c39a1-110">EXAMPLES</span></span>

### <span data-ttu-id="c39a1-111">예제 1: 대시보드 서식 파일을 사용 하 여 대시보드 만들기</span><span class="sxs-lookup"><span data-stu-id="c39a1-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="c39a1-112">제공 된 대시보드 서식 파일을 사용 하 여 새 대시보드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="c39a1-113">변수</span><span class="sxs-lookup"><span data-stu-id="c39a1-113">PARAMETERS</span></span>

### <span data-ttu-id="c39a1-114">-대시보드</span><span class="sxs-lookup"><span data-stu-id="c39a1-114">-Dashboard</span></span>
<span data-ttu-id="c39a1-115">공유 대시보드 리소스 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="c39a1-116">생성 하려면 대시보드 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="c39a1-117">-일점 보드 경로</span><span class="sxs-lookup"><span data-stu-id="c39a1-117">-DashboardPath</span></span>
<span data-ttu-id="c39a1-118">기존 대시보드 서식 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="c39a1-119">포털에서 대시보드 서식 파일을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="c39a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39a1-120">-DefaultProfile</span></span>
<span data-ttu-id="c39a1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c39a1-122">-렌즈</span><span class="sxs-lookup"><span data-stu-id="c39a1-122">-Lens</span></span>
<span data-ttu-id="c39a1-123">대시보드 렌즈.</span><span class="sxs-lookup"><span data-stu-id="c39a1-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="c39a1-124">-위치</span><span class="sxs-lookup"><span data-stu-id="c39a1-124">-Location</span></span>
<span data-ttu-id="c39a1-125">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="c39a1-125">Resource location</span></span>

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

### <span data-ttu-id="c39a1-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c39a1-126">-Metadata</span></span>
<span data-ttu-id="c39a1-127">대시보드 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="c39a1-128">-이름</span><span class="sxs-lookup"><span data-stu-id="c39a1-128">-Name</span></span>
<span data-ttu-id="c39a1-129">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="c39a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="c39a1-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="c39a1-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c39a1-132">-SubscriptionId</span></span>
<span data-ttu-id="c39a1-133">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-133">The Azure subscription ID.</span></span>
<span data-ttu-id="c39a1-134">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="c39a1-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c39a1-135">태그</span><span class="sxs-lookup"><span data-stu-id="c39a1-135">-Tag</span></span>
<span data-ttu-id="c39a1-136">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="c39a1-136">Resource tags</span></span>

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

### <span data-ttu-id="c39a1-137">-확인</span><span class="sxs-lookup"><span data-stu-id="c39a1-137">-Confirm</span></span>
<span data-ttu-id="c39a1-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39a1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39a1-139">-WhatIf</span></span>
<span data-ttu-id="c39a1-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39a1-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39a1-142">CommonParameters</span></span>
<span data-ttu-id="c39a1-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39a1-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c39a1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39a1-145">입력</span><span class="sxs-lookup"><span data-stu-id="c39a1-145">INPUTS</span></span>

### <span data-ttu-id="c39a1-146">Api201901Preview. i i m. i m a. i m a. i a Idashboard</span><span class="sxs-lookup"><span data-stu-id="c39a1-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="c39a1-147">출력</span><span class="sxs-lookup"><span data-stu-id="c39a1-147">OUTPUTS</span></span>

### <span data-ttu-id="c39a1-148">Api201901Preview. i i m. i m a. i m a. i a Idashboard</span><span class="sxs-lookup"><span data-stu-id="c39a1-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="c39a1-149">상속자</span><span class="sxs-lookup"><span data-stu-id="c39a1-149">NOTES</span></span>

<span data-ttu-id="c39a1-150">별칭과</span><span class="sxs-lookup"><span data-stu-id="c39a1-150">ALIASES</span></span>

<span data-ttu-id="c39a1-151">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c39a1-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c39a1-152">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c39a1-153">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c39a1-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c39a1-154">대시보드 <IDashboard> : 공유 대시보드 리소스 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="c39a1-155">`Location <String>`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="c39a1-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="c39a1-156">`[Lens <IDashboardPropertiesLenses>]`: 대시보드 렌즈.</span><span class="sxs-lookup"><span data-stu-id="c39a1-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="c39a1-157">`[(Any) <IDashboardLens>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c39a1-158">`[Metadata <IDashboardPropertiesMetadata>]`: 대시보드 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="c39a1-159">`[(Any) <Object>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c39a1-160">`[Tag <IDashboardTags>]`: 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="c39a1-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="c39a1-161">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c39a1-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="c39a1-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c39a1-162">RELATED LINKS</span></span>

