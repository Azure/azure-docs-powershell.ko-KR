---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304817"
---
# <span data-ttu-id="a8a1f-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="a8a1f-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="a8a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a1f-103">지정 된 응용 프로그램 그룹의 시작 메뉴 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="a8a1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8a1f-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a8a1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a1f-106">지정 된 응용 프로그램 그룹의 시작 메뉴 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="a8a1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a8a1f-107">EXAMPLES</span></span>

### <span data-ttu-id="a8a1f-108">예제 2: Windows 가상 데스크톱 시작 메뉴 항목 나열</span><span class="sxs-lookup"><span data-stu-id="a8a1f-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="a8a1f-109">이 명령은 applicaton 그룹의 Windows 가상 데스크톱 시작 메뉴 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="a8a1f-110">변수</span><span class="sxs-lookup"><span data-stu-id="a8a1f-110">PARAMETERS</span></span>

### <span data-ttu-id="a8a1f-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a1f-111">-ApplicationGroupName</span></span>
<span data-ttu-id="a8a1f-112">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-112">The name of the application group</span></span>

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

### <span data-ttu-id="a8a1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a1f-113">-DefaultProfile</span></span>
<span data-ttu-id="a8a1f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8a1f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a1f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a8a1f-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-116">The name of the resource group.</span></span>
<span data-ttu-id="a8a1f-117">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a8a1f-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8a1f-118">-SubscriptionId</span></span>
<span data-ttu-id="a8a1f-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a8a1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a1f-120">CommonParameters</span></span>
<span data-ttu-id="a8a1f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a1f-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8a1f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a1f-123">입력</span><span class="sxs-lookup"><span data-stu-id="a8a1f-123">INPUTS</span></span>

## <span data-ttu-id="a8a1f-124">출력</span><span class="sxs-lookup"><span data-stu-id="a8a1f-124">OUTPUTS</span></span>

### <span data-ttu-id="a8a1f-125">Api20191210Preview를 시작 하는 경우의 IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="a8a1f-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="a8a1f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="a8a1f-126">NOTES</span></span>

<span data-ttu-id="a8a1f-127">별칭과</span><span class="sxs-lookup"><span data-stu-id="a8a1f-127">ALIASES</span></span>

## <span data-ttu-id="a8a1f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8a1f-128">RELATED LINKS</span></span>

