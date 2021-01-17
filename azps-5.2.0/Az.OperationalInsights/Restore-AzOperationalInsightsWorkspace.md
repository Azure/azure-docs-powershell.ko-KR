---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337574"
---
# <span data-ttu-id="43e4b-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="43e4b-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="43e4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="43e4b-103">삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="43e4b-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="43e4b-104">구문</span><span class="sxs-lookup"><span data-stu-id="43e4b-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43e4b-105">설명</span><span class="sxs-lookup"><span data-stu-id="43e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="43e4b-106">삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="43e4b-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="43e4b-107">예제</span><span class="sxs-lookup"><span data-stu-id="43e4b-107">EXAMPLES</span></span>

### <span data-ttu-id="43e4b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="43e4b-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="43e4b-109">삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="43e4b-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="43e4b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43e4b-110">PARAMETERS</span></span>

### <span data-ttu-id="43e4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e4b-111">-DefaultProfile</span></span>
<span data-ttu-id="43e4b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e4b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="43e4b-113">-Force</span></span>
<span data-ttu-id="43e4b-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="43e4b-115">-Location</span><span class="sxs-lookup"><span data-stu-id="43e4b-115">-Location</span></span>
<span data-ttu-id="43e4b-116">작업 영역이 생성될 지리적 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e4b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43e4b-117">-Name</span></span>
<span data-ttu-id="43e4b-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e4b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e4b-119">-ResourceGroupName</span></span>
<span data-ttu-id="43e4b-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e4b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43e4b-121">-Confirm</span></span>
<span data-ttu-id="43e4b-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e4b-123">-WhatIf</span></span>
<span data-ttu-id="43e4b-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43e4b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e4b-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e4b-126">CommonParameters</span></span>
<span data-ttu-id="43e4b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e4b-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43e4b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e4b-129">입력</span><span class="sxs-lookup"><span data-stu-id="43e4b-129">INPUTS</span></span>

### <span data-ttu-id="43e4b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="43e4b-130">System.String</span></span>

## <span data-ttu-id="43e4b-131">출력</span><span class="sxs-lookup"><span data-stu-id="43e4b-131">OUTPUTS</span></span>

### <span data-ttu-id="43e4b-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="43e4b-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="43e4b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43e4b-133">NOTES</span></span>

## <span data-ttu-id="43e4b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43e4b-134">RELATED LINKS</span></span>
