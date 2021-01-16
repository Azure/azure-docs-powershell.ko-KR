---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341097"
---
# <span data-ttu-id="6c0cd-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="6c0cd-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="6c0cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0cd-103">Windows 가상 데스크톱 애플리케이션 그룹을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="6c0cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c0cd-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6c0cd-105">설명</span><span class="sxs-lookup"><span data-stu-id="6c0cd-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0cd-106">Windows 가상 데스크톱 애플리케이션 그룹을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="6c0cd-107">예제</span><span class="sxs-lookup"><span data-stu-id="6c0cd-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0cd-108">예제 1: Windows Virtual Desktop 애플리케이션 그룹 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="6c0cd-109">이 명령은 Windows Virtual Desktop 애플리케이션 그룹을 작업 영역으로 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="6c0cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c0cd-110">PARAMETERS</span></span>

### <span data-ttu-id="6c0cd-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="6c0cd-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="6c0cd-112">ResourceGroupName 경로</span><span class="sxs-lookup"><span data-stu-id="6c0cd-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="6c0cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0cd-113">-DefaultProfile</span></span>
<span data-ttu-id="6c0cd-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c0cd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0cd-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c0cd-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6c0cd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6c0cd-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c0cd-117">-SubscriptionId</span></span>
<span data-ttu-id="6c0cd-118">구독 ID</span><span class="sxs-lookup"><span data-stu-id="6c0cd-118">Subscription Id</span></span>

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

### <span data-ttu-id="6c0cd-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6c0cd-119">-WorkspaceName</span></span>
<span data-ttu-id="6c0cd-120">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="6c0cd-120">Workspace Name</span></span>

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

### <span data-ttu-id="6c0cd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c0cd-121">-Confirm</span></span>
<span data-ttu-id="6c0cd-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0cd-123">-WhatIf</span></span>
<span data-ttu-id="6c0cd-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6c0cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0cd-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0cd-126">CommonParameters</span></span>
<span data-ttu-id="6c0cd-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0cd-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c0cd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0cd-129">입력</span><span class="sxs-lookup"><span data-stu-id="6c0cd-129">INPUTS</span></span>

## <span data-ttu-id="6c0cd-130">출력</span><span class="sxs-lookup"><span data-stu-id="6c0cd-130">OUTPUTS</span></span>

### <span data-ttu-id="6c0cd-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c0cd-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="6c0cd-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c0cd-132">NOTES</span></span>

<span data-ttu-id="6c0cd-133">별칭</span><span class="sxs-lookup"><span data-stu-id="6c0cd-133">ALIASES</span></span>

## <span data-ttu-id="6c0cd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c0cd-134">RELATED LINKS</span></span>

