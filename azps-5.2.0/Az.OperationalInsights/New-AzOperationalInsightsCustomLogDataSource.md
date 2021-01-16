---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322741"
---
# <span data-ttu-id="bafbd-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="bafbd-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="bafbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bafbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bafbd-103">사용자 지정 로그 컬렉션 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="bafbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="bafbd-104">SYNTAX</span></span>

### <span data-ttu-id="bafbd-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bafbd-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafbd-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bafbd-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bafbd-107">설명</span><span class="sxs-lookup"><span data-stu-id="bafbd-107">DESCRIPTION</span></span>
<span data-ttu-id="bafbd-108">**New-AzOperationalInsightsCustomLogDataSource** cmdlet은 사용자 지정 로그 컬렉션 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="bafbd-109">예제</span><span class="sxs-lookup"><span data-stu-id="bafbd-109">EXAMPLES</span></span>

## <span data-ttu-id="bafbd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bafbd-110">PARAMETERS</span></span>

### <span data-ttu-id="bafbd-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="bafbd-111">-CustomLogRawJson</span></span>
<span data-ttu-id="bafbd-112">사용자 지정 컬렉션 정책을 원시 JSON(JavaScript Object Notation) 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="bafbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafbd-113">-DefaultProfile</span></span>
<span data-ttu-id="bafbd-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bafbd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bafbd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bafbd-115">-Force</span></span>
<span data-ttu-id="bafbd-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bafbd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bafbd-117">-Name</span></span>
<span data-ttu-id="bafbd-118">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="bafbd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafbd-119">-ResourceGroupName</span></span>
<span data-ttu-id="bafbd-120">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="bafbd-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="bafbd-121">-Workspace</span></span>
<span data-ttu-id="bafbd-122">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bafbd-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bafbd-123">-WorkspaceName</span></span>
<span data-ttu-id="bafbd-124">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bafbd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bafbd-125">-Confirm</span></span>
<span data-ttu-id="bafbd-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafbd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafbd-127">-WhatIf</span></span>
<span data-ttu-id="bafbd-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bafbd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafbd-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafbd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafbd-130">CommonParameters</span></span>
<span data-ttu-id="bafbd-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bafbd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafbd-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bafbd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafbd-133">입력</span><span class="sxs-lookup"><span data-stu-id="bafbd-133">INPUTS</span></span>

### <span data-ttu-id="bafbd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bafbd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bafbd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bafbd-135">System.String</span></span>

## <span data-ttu-id="bafbd-136">출력</span><span class="sxs-lookup"><span data-stu-id="bafbd-136">OUTPUTS</span></span>

### <span data-ttu-id="bafbd-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bafbd-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bafbd-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bafbd-138">NOTES</span></span>

## <span data-ttu-id="bafbd-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bafbd-139">RELATED LINKS</span></span>

[<span data-ttu-id="bafbd-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bafbd-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="bafbd-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bafbd-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


