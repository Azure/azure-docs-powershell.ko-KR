---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1035d918870a15000be066fd59cc72913d8d8cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989753"
---
# <span data-ttu-id="a806e-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a806e-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a806e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a806e-102">SYNOPSIS</span></span>
<span data-ttu-id="a806e-103">삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="a806e-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="a806e-104">구문</span><span class="sxs-lookup"><span data-stu-id="a806e-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a806e-105">설명</span><span class="sxs-lookup"><span data-stu-id="a806e-105">DESCRIPTION</span></span>
<span data-ttu-id="a806e-106">삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="a806e-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="a806e-107">예제</span><span class="sxs-lookup"><span data-stu-id="a806e-107">EXAMPLES</span></span>

### <span data-ttu-id="a806e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a806e-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="a806e-109">삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="a806e-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="a806e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a806e-110">PARAMETERS</span></span>

### <span data-ttu-id="a806e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a806e-111">-DefaultProfile</span></span>
<span data-ttu-id="a806e-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a806e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a806e-113">-Force</span></span>
<span data-ttu-id="a806e-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a806e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a806e-115">-Location</span></span>
<span data-ttu-id="a806e-116">작업 영역이 생성될 지리적 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="a806e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a806e-117">-Name</span></span>
<span data-ttu-id="a806e-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-118">The workspace name.</span></span>

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

### <span data-ttu-id="a806e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a806e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a806e-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-120">The resource group name.</span></span>

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

### <span data-ttu-id="a806e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="a806e-121">-Confirm</span></span>
<span data-ttu-id="a806e-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a806e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a806e-123">-WhatIf</span></span>
<span data-ttu-id="a806e-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a806e-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a806e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a806e-126">CommonParameters</span></span>
<span data-ttu-id="a806e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a806e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a806e-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a806e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a806e-129">입력</span><span class="sxs-lookup"><span data-stu-id="a806e-129">INPUTS</span></span>

### <span data-ttu-id="a806e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a806e-130">System.String</span></span>

## <span data-ttu-id="a806e-131">출력</span><span class="sxs-lookup"><span data-stu-id="a806e-131">OUTPUTS</span></span>

### <span data-ttu-id="a806e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a806e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a806e-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a806e-133">NOTES</span></span>

## <span data-ttu-id="a806e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a806e-134">RELATED LINKS</span></span>
