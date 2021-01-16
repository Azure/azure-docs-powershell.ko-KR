---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490899"
---
# <span data-ttu-id="08604-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="08604-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="08604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08604-102">SYNOPSIS</span></span>
<span data-ttu-id="08604-103">Windows 운영 체제를 실행하고 있는 연결된 컴퓨터에 대한 Windows 성능 카운터 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="08604-104">구문</span><span class="sxs-lookup"><span data-stu-id="08604-104">SYNTAX</span></span>

### <span data-ttu-id="08604-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="08604-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08604-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="08604-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08604-107">설명</span><span class="sxs-lookup"><span data-stu-id="08604-107">DESCRIPTION</span></span>
<span data-ttu-id="08604-108">**New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet은 Windows 운영 체제를 실행하고 있는 연결된 컴퓨터에 대한 Windows 성능 카운터 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="08604-109">예제</span><span class="sxs-lookup"><span data-stu-id="08604-109">EXAMPLES</span></span>

## <span data-ttu-id="08604-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08604-110">PARAMETERS</span></span>

### <span data-ttu-id="08604-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="08604-111">-CounterName</span></span>
<span data-ttu-id="08604-112">카운터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08604-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08604-113">-DefaultProfile</span></span>
<span data-ttu-id="08604-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08604-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08604-115">-Force</span><span class="sxs-lookup"><span data-stu-id="08604-115">-Force</span></span>
<span data-ttu-id="08604-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08604-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="08604-117">-InstanceName</span></span>
<span data-ttu-id="08604-118">인스턴스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="08604-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="08604-119">-IntervalSeconds</span></span>
<span data-ttu-id="08604-120">컬렉션 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="08604-121">-Name</span><span class="sxs-lookup"><span data-stu-id="08604-121">-Name</span></span>
<span data-ttu-id="08604-122">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="08604-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="08604-123">-ObjectName</span></span>
<span data-ttu-id="08604-124">개체의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="08604-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08604-125">-ResourceGroupName</span></span>
<span data-ttu-id="08604-126">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="08604-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="08604-127">-UseLegacyCollector</span></span>
<span data-ttu-id="08604-128">레거시 수집기 또는 기본 수집기 사용.</span><span class="sxs-lookup"><span data-stu-id="08604-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="08604-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="08604-129">-Workspace</span></span>
<span data-ttu-id="08604-130">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="08604-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="08604-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08604-131">-WorkspaceName</span></span>
<span data-ttu-id="08604-132">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="08604-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08604-133">-Confirm</span></span>
<span data-ttu-id="08604-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08604-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08604-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08604-135">-WhatIf</span></span>
<span data-ttu-id="08604-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="08604-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08604-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08604-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08604-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08604-138">CommonParameters</span></span>
<span data-ttu-id="08604-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08604-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08604-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="08604-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08604-141">입력</span><span class="sxs-lookup"><span data-stu-id="08604-141">INPUTS</span></span>

### <span data-ttu-id="08604-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="08604-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="08604-143">System.String</span><span class="sxs-lookup"><span data-stu-id="08604-143">System.String</span></span>

### <span data-ttu-id="08604-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="08604-144">System.Int32</span></span>

## <span data-ttu-id="08604-145">출력</span><span class="sxs-lookup"><span data-stu-id="08604-145">OUTPUTS</span></span>

### <span data-ttu-id="08604-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="08604-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="08604-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08604-147">NOTES</span></span>

## <span data-ttu-id="08604-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08604-148">RELATED LINKS</span></span>
