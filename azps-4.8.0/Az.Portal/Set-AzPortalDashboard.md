---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214291"
---
# <span data-ttu-id="e225a-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="e225a-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="e225a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e225a-102">SYNOPSIS</span></span>
<span data-ttu-id="e225a-103">대시보드를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="e225a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e225a-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e225a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e225a-105">DESCRIPTION</span></span>
<span data-ttu-id="e225a-106">대시보드를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="e225a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e225a-107">EXAMPLES</span></span>

### <span data-ttu-id="e225a-108">예제 1: 대시보드 서식 파일을 사용 하 여 대시보드 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="e225a-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="e225a-109">Dashbaord 서식 파일을 사용 하 여 대시보드 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="e225a-110">변수</span><span class="sxs-lookup"><span data-stu-id="e225a-110">PARAMETERS</span></span>

### <span data-ttu-id="e225a-111">-일점 보드 경로</span><span class="sxs-lookup"><span data-stu-id="e225a-111">-DashboardPath</span></span>
<span data-ttu-id="e225a-112">기존 대시보드 서식 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="e225a-113">포털에서 대시보드 서식 파일을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="e225a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e225a-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="e225a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e225a-115">-Name</span></span>


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

### <span data-ttu-id="e225a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e225a-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="e225a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e225a-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="e225a-118">-확인</span><span class="sxs-lookup"><span data-stu-id="e225a-118">-Confirm</span></span>
<span data-ttu-id="e225a-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e225a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e225a-120">-WhatIf</span></span>
<span data-ttu-id="e225a-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e225a-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e225a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e225a-123">CommonParameters</span></span>
<span data-ttu-id="e225a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e225a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e225a-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e225a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e225a-126">입력</span><span class="sxs-lookup"><span data-stu-id="e225a-126">INPUTS</span></span>

## <span data-ttu-id="e225a-127">출력</span><span class="sxs-lookup"><span data-stu-id="e225a-127">OUTPUTS</span></span>

### <span data-ttu-id="e225a-128">Api201901Preview. i i m. i m a. i m a. i a Idashboard</span><span class="sxs-lookup"><span data-stu-id="e225a-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="e225a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e225a-129">NOTES</span></span>

<span data-ttu-id="e225a-130">별칭과</span><span class="sxs-lookup"><span data-stu-id="e225a-130">ALIASES</span></span>

## <span data-ttu-id="e225a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e225a-131">RELATED LINKS</span></span>

