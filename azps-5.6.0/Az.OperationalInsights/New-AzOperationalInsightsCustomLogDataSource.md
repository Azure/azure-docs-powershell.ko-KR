---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e923d413b889583578efb0ac81f9eb6aeadf72fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977808"
---
# <span data-ttu-id="fcab8-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="fcab8-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="fcab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcab8-102">SYNOPSIS</span></span>
<span data-ttu-id="fcab8-103">사용자 지정 로그 수집 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="fcab8-104">구문</span><span class="sxs-lookup"><span data-stu-id="fcab8-104">SYNTAX</span></span>

### <span data-ttu-id="fcab8-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fcab8-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcab8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fcab8-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcab8-107">설명</span><span class="sxs-lookup"><span data-stu-id="fcab8-107">DESCRIPTION</span></span>
<span data-ttu-id="fcab8-108">**New-AzOperationalInsightsCustomLogDataSource** cmdlet은 사용자 지정 로그 수집 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="fcab8-109">예제</span><span class="sxs-lookup"><span data-stu-id="fcab8-109">EXAMPLES</span></span>

## <span data-ttu-id="fcab8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fcab8-110">PARAMETERS</span></span>

### <span data-ttu-id="fcab8-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="fcab8-111">-CustomLogRawJson</span></span>
<span data-ttu-id="fcab8-112">사용자 지정 컬렉션 정책을 원시 JavaScript 개체 표기(JSON) 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="fcab8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcab8-113">-DefaultProfile</span></span>
<span data-ttu-id="fcab8-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fcab8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcab8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fcab8-115">-Force</span></span>
<span data-ttu-id="fcab8-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fcab8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fcab8-117">-Name</span></span>
<span data-ttu-id="fcab8-118">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="fcab8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcab8-119">-ResourceGroupName</span></span>
<span data-ttu-id="fcab8-120">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="fcab8-121">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="fcab8-121">-Workspace</span></span>
<span data-ttu-id="fcab8-122">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fcab8-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fcab8-123">-WorkspaceName</span></span>
<span data-ttu-id="fcab8-124">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fcab8-125">-확인</span><span class="sxs-lookup"><span data-stu-id="fcab8-125">-Confirm</span></span>
<span data-ttu-id="fcab8-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcab8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcab8-127">-WhatIf</span></span>
<span data-ttu-id="fcab8-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcab8-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcab8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcab8-130">CommonParameters</span></span>
<span data-ttu-id="fcab8-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fcab8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcab8-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fcab8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcab8-133">입력</span><span class="sxs-lookup"><span data-stu-id="fcab8-133">INPUTS</span></span>

### <span data-ttu-id="fcab8-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fcab8-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fcab8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fcab8-135">System.String</span></span>

## <span data-ttu-id="fcab8-136">출력</span><span class="sxs-lookup"><span data-stu-id="fcab8-136">OUTPUTS</span></span>

### <span data-ttu-id="fcab8-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fcab8-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fcab8-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fcab8-138">NOTES</span></span>

## <span data-ttu-id="fcab8-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcab8-139">RELATED LINKS</span></span>

[<span data-ttu-id="fcab8-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fcab8-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="fcab8-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fcab8-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


