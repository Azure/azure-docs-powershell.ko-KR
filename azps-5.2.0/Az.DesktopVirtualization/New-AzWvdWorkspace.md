---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: a9fc9a4900b7e11fddb01e47fbcf1c5407926749
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338457"
---
# <span data-ttu-id="34986-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="34986-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="34986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34986-102">SYNOPSIS</span></span>
<span data-ttu-id="34986-103">작업 영역 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="34986-103">Create or update a workspace.</span></span>

## <span data-ttu-id="34986-104">구문</span><span class="sxs-lookup"><span data-stu-id="34986-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34986-105">설명</span><span class="sxs-lookup"><span data-stu-id="34986-105">DESCRIPTION</span></span>
<span data-ttu-id="34986-106">작업 영역 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="34986-106">Create or update a workspace.</span></span>

## <span data-ttu-id="34986-107">예제</span><span class="sxs-lookup"><span data-stu-id="34986-107">EXAMPLES</span></span>

### <span data-ttu-id="34986-108">예제 1: 이름으로 Windows Virtual Desktop 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="34986-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="34986-109">이 명령은 리소스 그룹에 Windows Virtual Desktop 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="34986-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="34986-110">예제 2: 이름으로 Windows Virtual Desktop 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="34986-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="34986-111">이 명령은 리소스 그룹에 Windows Virtual Desktop 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="34986-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="34986-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34986-112">PARAMETERS</span></span>

### <span data-ttu-id="34986-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="34986-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="34986-114">applicationGroup 리소스 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="34986-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="34986-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34986-115">-DefaultProfile</span></span>
<span data-ttu-id="34986-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34986-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34986-117">-Description</span><span class="sxs-lookup"><span data-stu-id="34986-117">-Description</span></span>
<span data-ttu-id="34986-118">작업 영역의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="34986-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="34986-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="34986-119">-FriendlyName</span></span>
<span data-ttu-id="34986-120">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34986-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="34986-121">-Location</span><span class="sxs-lookup"><span data-stu-id="34986-121">-Location</span></span>
<span data-ttu-id="34986-122">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="34986-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="34986-123">-Name</span><span class="sxs-lookup"><span data-stu-id="34986-123">-Name</span></span>
<span data-ttu-id="34986-124">작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="34986-124">The name of the workspace</span></span>

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

### <span data-ttu-id="34986-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34986-125">-ResourceGroupName</span></span>
<span data-ttu-id="34986-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34986-126">The name of the resource group.</span></span>
<span data-ttu-id="34986-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="34986-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34986-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34986-128">-SubscriptionId</span></span>
<span data-ttu-id="34986-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="34986-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34986-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="34986-130">-Tag</span></span>
<span data-ttu-id="34986-131">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="34986-131">Resource tags.</span></span>

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

### <span data-ttu-id="34986-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34986-132">-Confirm</span></span>
<span data-ttu-id="34986-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34986-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34986-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34986-134">-WhatIf</span></span>
<span data-ttu-id="34986-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="34986-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34986-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34986-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34986-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34986-137">CommonParameters</span></span>
<span data-ttu-id="34986-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34986-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34986-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34986-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34986-140">입력</span><span class="sxs-lookup"><span data-stu-id="34986-140">INPUTS</span></span>

## <span data-ttu-id="34986-141">출력</span><span class="sxs-lookup"><span data-stu-id="34986-141">OUTPUTS</span></span>

### <span data-ttu-id="34986-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="34986-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="34986-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34986-143">NOTES</span></span>

<span data-ttu-id="34986-144">별칭</span><span class="sxs-lookup"><span data-stu-id="34986-144">ALIASES</span></span>

## <span data-ttu-id="34986-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34986-145">RELATED LINKS</span></span>

