---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980560"
---
# <span data-ttu-id="c25a9-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="c25a9-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="c25a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25a9-102">SYNOPSIS</span></span>
<span data-ttu-id="c25a9-103">주어진 애플리케이션 그룹에 시작 메뉴 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="c25a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="c25a9-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c25a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="c25a9-105">DESCRIPTION</span></span>
<span data-ttu-id="c25a9-106">주어진 애플리케이션 그룹에 시작 메뉴 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="c25a9-107">예제</span><span class="sxs-lookup"><span data-stu-id="c25a9-107">EXAMPLES</span></span>

### <span data-ttu-id="c25a9-108">예제 2: Windows Virtual Desktop 시작 메뉴 항목 나열</span><span class="sxs-lookup"><span data-stu-id="c25a9-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="c25a9-109">이 명령은 해당 그룹의 Windows Virtual Desktop 시작 메뉴 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="c25a9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c25a9-110">PARAMETERS</span></span>

### <span data-ttu-id="c25a9-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="c25a9-111">-ApplicationGroupName</span></span>
<span data-ttu-id="c25a9-112">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c25a9-112">The name of the application group</span></span>

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

### <span data-ttu-id="c25a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25a9-113">-DefaultProfile</span></span>
<span data-ttu-id="c25a9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="c25a9-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-116">The name of the resource group.</span></span>
<span data-ttu-id="c25a9-117">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c25a9-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c25a9-118">-SubscriptionId</span></span>
<span data-ttu-id="c25a9-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25a9-120">CommonParameters</span></span>
<span data-ttu-id="c25a9-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25a9-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c25a9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25a9-123">입력</span><span class="sxs-lookup"><span data-stu-id="c25a9-123">INPUTS</span></span>

## <span data-ttu-id="c25a9-124">출력</span><span class="sxs-lookup"><span data-stu-id="c25a9-124">OUTPUTS</span></span>

### <span data-ttu-id="c25a9-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="c25a9-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="c25a9-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c25a9-126">NOTES</span></span>

<span data-ttu-id="c25a9-127">별칭</span><span class="sxs-lookup"><span data-stu-id="c25a9-127">ALIASES</span></span>

## <span data-ttu-id="c25a9-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c25a9-128">RELATED LINKS</span></span>

