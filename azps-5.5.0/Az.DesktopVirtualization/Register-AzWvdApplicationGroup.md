---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204245"
---
# <span data-ttu-id="f662c-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f662c-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f662c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f662c-102">SYNOPSIS</span></span>
<span data-ttu-id="f662c-103">Windows 가상 데스크톱 애플리케이션 그룹을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="f662c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f662c-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f662c-105">설명</span><span class="sxs-lookup"><span data-stu-id="f662c-105">DESCRIPTION</span></span>
<span data-ttu-id="f662c-106">Windows 가상 데스크톱 애플리케이션 그룹을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="f662c-107">예제</span><span class="sxs-lookup"><span data-stu-id="f662c-107">EXAMPLES</span></span>

### <span data-ttu-id="f662c-108">예제 1: Windows Virtual Desktop 애플리케이션 그룹 등록</span><span class="sxs-lookup"><span data-stu-id="f662c-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="f662c-109">이 명령은 Windows Virtual Desktop 애플리케이션 그룹을 작업 영역으로 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="f662c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f662c-110">PARAMETERS</span></span>

### <span data-ttu-id="f662c-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="f662c-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="f662c-112">ApplicationGroupPath 경로</span><span class="sxs-lookup"><span data-stu-id="f662c-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="f662c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f662c-113">-DefaultProfile</span></span>
<span data-ttu-id="f662c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f662c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f662c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f662c-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f662c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f662c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f662c-117">-SubscriptionId</span></span>
<span data-ttu-id="f662c-118">구독 ID</span><span class="sxs-lookup"><span data-stu-id="f662c-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f662c-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f662c-119">-WorkspaceName</span></span>
<span data-ttu-id="f662c-120">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="f662c-120">Workspace Name</span></span>

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

### <span data-ttu-id="f662c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f662c-121">-Confirm</span></span>
<span data-ttu-id="f662c-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f662c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f662c-123">-WhatIf</span></span>
<span data-ttu-id="f662c-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f662c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f662c-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f662c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f662c-126">CommonParameters</span></span>
<span data-ttu-id="f662c-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f662c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f662c-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f662c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f662c-129">입력</span><span class="sxs-lookup"><span data-stu-id="f662c-129">INPUTS</span></span>

## <span data-ttu-id="f662c-130">출력</span><span class="sxs-lookup"><span data-stu-id="f662c-130">OUTPUTS</span></span>

### <span data-ttu-id="f662c-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="f662c-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="f662c-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f662c-132">NOTES</span></span>

<span data-ttu-id="f662c-133">별칭</span><span class="sxs-lookup"><span data-stu-id="f662c-133">ALIASES</span></span>

## <span data-ttu-id="f662c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f662c-134">RELATED LINKS</span></span>

