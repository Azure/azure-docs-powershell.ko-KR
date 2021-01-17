---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345842"
---
# <span data-ttu-id="f0322-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f0322-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="f0322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0322-102">SYNOPSIS</span></span>
<span data-ttu-id="f0322-103">Linux 컴퓨터에서 성능 카운터 컬렉션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="f0322-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0322-104">SYNTAX</span></span>

### <span data-ttu-id="f0322-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f0322-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0322-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f0322-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0322-107">설명</span><span class="sxs-lookup"><span data-stu-id="f0322-107">DESCRIPTION</span></span>
<span data-ttu-id="f0322-108">**Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet은 작업 영역의 연결된 Linux 컴퓨터에서 성능 카운터 컬렉션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="f0322-109">예제</span><span class="sxs-lookup"><span data-stu-id="f0322-109">EXAMPLES</span></span>

## <span data-ttu-id="f0322-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0322-110">PARAMETERS</span></span>

### <span data-ttu-id="f0322-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0322-111">-DefaultProfile</span></span>
<span data-ttu-id="f0322-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f0322-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0322-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0322-113">-ResourceGroupName</span></span>
<span data-ttu-id="f0322-114">Linux 컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="f0322-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f0322-115">-Workspace</span></span>
<span data-ttu-id="f0322-116">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f0322-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f0322-117">-WorkspaceName</span></span>
<span data-ttu-id="f0322-118">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f0322-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0322-119">-Confirm</span></span>
<span data-ttu-id="f0322-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0322-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0322-121">-WhatIf</span></span>
<span data-ttu-id="f0322-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f0322-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0322-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0322-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0322-124">CommonParameters</span></span>
<span data-ttu-id="f0322-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0322-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0322-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0322-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0322-127">입력</span><span class="sxs-lookup"><span data-stu-id="f0322-127">INPUTS</span></span>

### <span data-ttu-id="f0322-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0322-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f0322-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f0322-129">System.String</span></span>

## <span data-ttu-id="f0322-130">출력</span><span class="sxs-lookup"><span data-stu-id="f0322-130">OUTPUTS</span></span>

### <span data-ttu-id="f0322-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f0322-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f0322-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0322-132">NOTES</span></span>
* <span data-ttu-id="f0322-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="f0322-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f0322-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0322-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0322-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="f0322-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


