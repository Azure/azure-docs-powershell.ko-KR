---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331257"
---
# <span data-ttu-id="da0bb-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="da0bb-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="da0bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da0bb-102">SYNOPSIS</span></span>
<span data-ttu-id="da0bb-103">대시보드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="da0bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="da0bb-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da0bb-105">설명</span><span class="sxs-lookup"><span data-stu-id="da0bb-105">DESCRIPTION</span></span>
<span data-ttu-id="da0bb-106">대시보드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="da0bb-107">예제</span><span class="sxs-lookup"><span data-stu-id="da0bb-107">EXAMPLES</span></span>

### <span data-ttu-id="da0bb-108">예제 1: 대시보드 템플릿을 사용하여 대시보드 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="da0bb-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="da0bb-109">대시베이어 템플릿 파일을 사용하여 대시보드 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="da0bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da0bb-110">PARAMETERS</span></span>

### <span data-ttu-id="da0bb-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="da0bb-111">-DashboardPath</span></span>
<span data-ttu-id="da0bb-112">기존 대시보드 템플릿에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="da0bb-113">대시보드 템플릿은 포털에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="da0bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0bb-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="da0bb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="da0bb-115">-Name</span></span>


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

### <span data-ttu-id="da0bb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0bb-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="da0bb-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da0bb-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="da0bb-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da0bb-118">-Confirm</span></span>
<span data-ttu-id="da0bb-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0bb-120">-WhatIf</span></span>
<span data-ttu-id="da0bb-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da0bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da0bb-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0bb-123">CommonParameters</span></span>
<span data-ttu-id="da0bb-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da0bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0bb-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da0bb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0bb-126">입력</span><span class="sxs-lookup"><span data-stu-id="da0bb-126">INPUTS</span></span>

## <span data-ttu-id="da0bb-127">출력</span><span class="sxs-lookup"><span data-stu-id="da0bb-127">OUTPUTS</span></span>

### <span data-ttu-id="da0bb-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="da0bb-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="da0bb-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da0bb-129">NOTES</span></span>

<span data-ttu-id="da0bb-130">별칭</span><span class="sxs-lookup"><span data-stu-id="da0bb-130">ALIASES</span></span>

## <span data-ttu-id="da0bb-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da0bb-131">RELATED LINKS</span></span>

