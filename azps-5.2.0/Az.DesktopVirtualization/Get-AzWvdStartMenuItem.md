---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: 4ad2b7db5e212cf15748ac81ae28b9471d1678b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354206"
---
# <span data-ttu-id="8406d-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="8406d-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="8406d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8406d-102">SYNOPSIS</span></span>
<span data-ttu-id="8406d-103">주어진 애플리케이션 그룹의 시작 메뉴 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="8406d-104">구문</span><span class="sxs-lookup"><span data-stu-id="8406d-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8406d-105">설명</span><span class="sxs-lookup"><span data-stu-id="8406d-105">DESCRIPTION</span></span>
<span data-ttu-id="8406d-106">주어진 애플리케이션 그룹의 시작 메뉴 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="8406d-107">예제</span><span class="sxs-lookup"><span data-stu-id="8406d-107">EXAMPLES</span></span>

### <span data-ttu-id="8406d-108">예제 2: Windows Virtual Desktop 시작 메뉴 항목 나열</span><span class="sxs-lookup"><span data-stu-id="8406d-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="8406d-109">이 명령은 응용 프로그램 그룹의 Windows Virtual Desktop 시작 메뉴 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="8406d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8406d-110">PARAMETERS</span></span>

### <span data-ttu-id="8406d-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="8406d-111">-ApplicationGroupName</span></span>
<span data-ttu-id="8406d-112">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="8406d-112">The name of the application group</span></span>

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

### <span data-ttu-id="8406d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8406d-113">-DefaultProfile</span></span>
<span data-ttu-id="8406d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8406d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8406d-115">-ResourceGroupName</span></span>
<span data-ttu-id="8406d-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-116">The name of the resource group.</span></span>
<span data-ttu-id="8406d-117">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8406d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8406d-118">-SubscriptionId</span></span>
<span data-ttu-id="8406d-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8406d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8406d-120">CommonParameters</span></span>
<span data-ttu-id="8406d-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8406d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8406d-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8406d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8406d-123">입력</span><span class="sxs-lookup"><span data-stu-id="8406d-123">INPUTS</span></span>

## <span data-ttu-id="8406d-124">출력</span><span class="sxs-lookup"><span data-stu-id="8406d-124">OUTPUTS</span></span>

### <span data-ttu-id="8406d-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="8406d-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IStartMenuItem</span></span>

## <span data-ttu-id="8406d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8406d-126">NOTES</span></span>

<span data-ttu-id="8406d-127">별칭</span><span class="sxs-lookup"><span data-stu-id="8406d-127">ALIASES</span></span>

## <span data-ttu-id="8406d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8406d-128">RELATED LINKS</span></span>

