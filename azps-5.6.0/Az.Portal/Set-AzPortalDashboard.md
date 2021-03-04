---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 8002a0a38353022c273aa680ccae9cf354b3540d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988955"
---
# <span data-ttu-id="25590-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="25590-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="25590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25590-102">SYNOPSIS</span></span>
<span data-ttu-id="25590-103">대시보드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="25590-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="25590-104">구문</span><span class="sxs-lookup"><span data-stu-id="25590-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25590-105">설명</span><span class="sxs-lookup"><span data-stu-id="25590-105">DESCRIPTION</span></span>
<span data-ttu-id="25590-106">대시보드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="25590-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="25590-107">예제</span><span class="sxs-lookup"><span data-stu-id="25590-107">EXAMPLES</span></span>

### <span data-ttu-id="25590-108">예제 1: 대시보드 템플릿을 사용하여 대시보드 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="25590-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="25590-109">dashbaord 템플릿 파일을 사용하여 대시보드 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="25590-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="25590-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="25590-110">PARAMETERS</span></span>

### <span data-ttu-id="25590-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="25590-111">-DashboardPath</span></span>
<span data-ttu-id="25590-112">기존 대시보드 템플릿에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="25590-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="25590-113">대시보드 템플릿은 포털에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25590-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="25590-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25590-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="25590-115">-Name</span><span class="sxs-lookup"><span data-stu-id="25590-115">-Name</span></span>


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

### <span data-ttu-id="25590-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25590-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="25590-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25590-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="25590-118">-확인</span><span class="sxs-lookup"><span data-stu-id="25590-118">-Confirm</span></span>
<span data-ttu-id="25590-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25590-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25590-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25590-120">-WhatIf</span></span>
<span data-ttu-id="25590-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="25590-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25590-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25590-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25590-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25590-123">CommonParameters</span></span>
<span data-ttu-id="25590-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25590-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25590-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25590-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25590-126">입력</span><span class="sxs-lookup"><span data-stu-id="25590-126">INPUTS</span></span>

## <span data-ttu-id="25590-127">출력</span><span class="sxs-lookup"><span data-stu-id="25590-127">OUTPUTS</span></span>

### <span data-ttu-id="25590-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="25590-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="25590-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25590-129">NOTES</span></span>

<span data-ttu-id="25590-130">별칭</span><span class="sxs-lookup"><span data-stu-id="25590-130">ALIASES</span></span>

## <span data-ttu-id="25590-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25590-131">RELATED LINKS</span></span>

