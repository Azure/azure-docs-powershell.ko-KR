---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215012"
---
# <span data-ttu-id="69b5d-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="69b5d-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="69b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="69b5d-103">작업 영역을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-103">Create or update a workspace.</span></span>

## <span data-ttu-id="69b5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69b5d-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69b5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="69b5d-106">작업 영역을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-106">Create or update a workspace.</span></span>

## <span data-ttu-id="69b5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="69b5d-108">예제 1: 이름으로 Windows 가상 데스크톱 Worksapce 만들기</span><span class="sxs-lookup"><span data-stu-id="69b5d-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="69b5d-109">이 명령은 리소스 그룹에 Windows 가상 데스크톱 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="69b5d-110">예제 2: 이름으로 Windows 가상 데스크톱 Worksapce 만들기</span><span class="sxs-lookup"><span data-stu-id="69b5d-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="69b5d-111">이 명령은 리소스 그룹에 Windows 가상 데스크톱 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="69b5d-112">변수</span><span class="sxs-lookup"><span data-stu-id="69b5d-112">PARAMETERS</span></span>

### <span data-ttu-id="69b5d-113">-ApplicationGroupReference 설정</span><span class="sxs-lookup"><span data-stu-id="69b5d-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="69b5d-114">ApplicationGroup 리소스 Id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b5d-115">-DefaultProfile</span></span>
<span data-ttu-id="69b5d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b5d-117">-설명</span><span class="sxs-lookup"><span data-stu-id="69b5d-117">-Description</span></span>
<span data-ttu-id="69b5d-118">작업 영역에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-118">Description of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b5d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="69b5d-119">-FriendlyName</span></span>
<span data-ttu-id="69b5d-120">작업 영역의 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-120">Friendly name of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b5d-121">-위치</span><span class="sxs-lookup"><span data-stu-id="69b5d-121">-Location</span></span>
<span data-ttu-id="69b5d-122">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="69b5d-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="69b5d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="69b5d-123">-Name</span></span>
<span data-ttu-id="69b5d-124">작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="69b5d-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="69b5d-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-126">The name of the resource group.</span></span>
<span data-ttu-id="69b5d-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="69b5d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69b5d-128">-SubscriptionId</span></span>
<span data-ttu-id="69b5d-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="69b5d-130">태그</span><span class="sxs-lookup"><span data-stu-id="69b5d-130">-Tag</span></span>
<span data-ttu-id="69b5d-131">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="69b5d-131">Resource tags.</span></span>

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

### <span data-ttu-id="69b5d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="69b5d-132">-Confirm</span></span>
<span data-ttu-id="69b5d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b5d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b5d-134">-WhatIf</span></span>
<span data-ttu-id="69b5d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b5d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b5d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b5d-137">CommonParameters</span></span>
<span data-ttu-id="69b5d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b5d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b5d-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69b5d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b5d-140">입력</span><span class="sxs-lookup"><span data-stu-id="69b5d-140">INPUTS</span></span>

## <span data-ttu-id="69b5d-141">출력</span><span class="sxs-lookup"><span data-stu-id="69b5d-141">OUTPUTS</span></span>

### <span data-ttu-id="69b5d-142">Api20191210Preview. i i m. .exe 작업 영역</span><span class="sxs-lookup"><span data-stu-id="69b5d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="69b5d-143">상속자</span><span class="sxs-lookup"><span data-stu-id="69b5d-143">NOTES</span></span>

<span data-ttu-id="69b5d-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="69b5d-144">ALIASES</span></span>

## <span data-ttu-id="69b5d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69b5d-145">RELATED LINKS</span></span>

