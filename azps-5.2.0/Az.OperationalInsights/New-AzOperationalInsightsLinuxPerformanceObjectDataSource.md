---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341637"
---
# <span data-ttu-id="8ed52-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="8ed52-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="8ed52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ed52-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed52-103">작업 영역의 모든 Linux 컴퓨터에 성능 카운터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="8ed52-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ed52-104">SYNTAX</span></span>

### <span data-ttu-id="8ed52-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8ed52-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed52-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8ed52-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed52-107">설명</span><span class="sxs-lookup"><span data-stu-id="8ed52-107">DESCRIPTION</span></span>
<span data-ttu-id="8ed52-108">**New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet은 Azure Operational Insights가 작업 영역의 모든 Linux 컴퓨터에 데이터를 수집하는 성능 카운터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="8ed52-109">예제</span><span class="sxs-lookup"><span data-stu-id="8ed52-109">EXAMPLES</span></span>

## <span data-ttu-id="8ed52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ed52-110">PARAMETERS</span></span>

### <span data-ttu-id="8ed52-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="8ed52-111">-CounterNames</span></span>
<span data-ttu-id="8ed52-112">카운터의 이름 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed52-113">-DefaultProfile</span></span>
<span data-ttu-id="8ed52-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8ed52-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ed52-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8ed52-115">-Force</span></span>
<span data-ttu-id="8ed52-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ed52-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8ed52-117">-InstanceName</span></span>
<span data-ttu-id="8ed52-118">인스턴스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed52-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8ed52-119">-IntervalSeconds</span></span>
<span data-ttu-id="8ed52-120">컬렉션 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed52-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8ed52-121">-Name</span></span>
<span data-ttu-id="8ed52-122">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="8ed52-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="8ed52-123">-ObjectName</span></span>
<span data-ttu-id="8ed52-124">개체의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="8ed52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed52-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ed52-126">Linux 컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="8ed52-127">-Workspace</span><span class="sxs-lookup"><span data-stu-id="8ed52-127">-Workspace</span></span>
<span data-ttu-id="8ed52-128">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ed52-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ed52-129">-WorkspaceName</span></span>
<span data-ttu-id="8ed52-130">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ed52-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ed52-131">-Confirm</span></span>
<span data-ttu-id="8ed52-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed52-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed52-133">-WhatIf</span></span>
<span data-ttu-id="8ed52-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8ed52-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ed52-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed52-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed52-136">CommonParameters</span></span>
<span data-ttu-id="8ed52-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed52-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed52-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8ed52-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed52-139">입력</span><span class="sxs-lookup"><span data-stu-id="8ed52-139">INPUTS</span></span>

### <span data-ttu-id="8ed52-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ed52-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8ed52-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8ed52-141">System.String</span></span>

### <span data-ttu-id="8ed52-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8ed52-142">System.String[]</span></span>

### <span data-ttu-id="8ed52-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8ed52-143">System.Int32</span></span>

## <span data-ttu-id="8ed52-144">출력</span><span class="sxs-lookup"><span data-stu-id="8ed52-144">OUTPUTS</span></span>

### <span data-ttu-id="8ed52-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8ed52-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8ed52-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ed52-146">NOTES</span></span>

## <span data-ttu-id="8ed52-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ed52-147">RELATED LINKS</span></span>

[<span data-ttu-id="8ed52-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8ed52-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="8ed52-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8ed52-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


