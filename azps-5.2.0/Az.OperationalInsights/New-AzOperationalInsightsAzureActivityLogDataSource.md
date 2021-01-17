---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356644"
---
# <span data-ttu-id="69df4-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="69df4-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="69df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69df4-102">SYNOPSIS</span></span>
<span data-ttu-id="69df4-103">주어진 구독에서 Azure 활동 로그를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="69df4-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="69df4-104">구문</span><span class="sxs-lookup"><span data-stu-id="69df4-104">SYNTAX</span></span>

### <span data-ttu-id="69df4-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="69df4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69df4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="69df4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69df4-107">설명</span><span class="sxs-lookup"><span data-stu-id="69df4-107">DESCRIPTION</span></span>
<span data-ttu-id="69df4-108">이 New-AzOperationalInsightsAzureActivityLogDataSource Log Analytics가 주어진 구독에서 Azure 활동 로그를 수집할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="69df4-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="69df4-109">예제</span><span class="sxs-lookup"><span data-stu-id="69df4-109">EXAMPLES</span></span>

### <span data-ttu-id="69df4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="69df4-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="69df4-111">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="69df4-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="69df4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69df4-112">PARAMETERS</span></span>

### <span data-ttu-id="69df4-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="69df4-113">-BackfillStartTime</span></span>
<span data-ttu-id="69df4-114">1주일 전에 로그를 백업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69df4-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69df4-115">-DefaultProfile</span></span>
<span data-ttu-id="69df4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="69df4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="69df4-117">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="69df4-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69df4-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69df4-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="69df4-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69df4-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69df4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69df4-123">-Confirm</span></span>
<span data-ttu-id="69df4-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="69df4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69df4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69df4-125">-WhatIf</span></span>
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

### <span data-ttu-id="69df4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69df4-126">CommonParameters</span></span>
<span data-ttu-id="69df4-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69df4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69df4-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="69df4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69df4-129">입력</span><span class="sxs-lookup"><span data-stu-id="69df4-129">INPUTS</span></span>

### <span data-ttu-id="69df4-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="69df4-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="69df4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="69df4-131">System.String</span></span>

### <span data-ttu-id="69df4-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69df4-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="69df4-133">출력</span><span class="sxs-lookup"><span data-stu-id="69df4-133">OUTPUTS</span></span>

### <span data-ttu-id="69df4-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="69df4-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="69df4-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69df4-135">NOTES</span></span>

## <span data-ttu-id="69df4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69df4-136">RELATED LINKS</span></span>
