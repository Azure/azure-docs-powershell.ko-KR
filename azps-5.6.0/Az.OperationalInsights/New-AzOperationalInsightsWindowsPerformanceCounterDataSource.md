---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 2e3cd573c337d7ff13401939aaf127fa64a6c765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989884"
---
# <span data-ttu-id="5a7c7-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="5a7c7-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="5a7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7c7-103">Windows 운영 체제를 실행하는 연결된 컴퓨터에 대한 Windows 성능 카운터 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="5a7c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a7c7-104">SYNTAX</span></span>

### <span data-ttu-id="5a7c7-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="5a7c7-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7c7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5a7c7-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a7c7-107">설명</span><span class="sxs-lookup"><span data-stu-id="5a7c7-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7c7-108">**New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet은 Windows 운영 체제를 실행하는 연결된 컴퓨터에 대한 Windows 성능 카운터 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="5a7c7-109">예제</span><span class="sxs-lookup"><span data-stu-id="5a7c7-109">EXAMPLES</span></span>

## <span data-ttu-id="5a7c7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a7c7-110">PARAMETERS</span></span>

### <span data-ttu-id="5a7c7-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="5a7c7-111">-CounterName</span></span>
<span data-ttu-id="5a7c7-112">카운터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="5a7c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7c7-113">-DefaultProfile</span></span>
<span data-ttu-id="5a7c7-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a7c7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a7c7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5a7c7-115">-Force</span></span>
<span data-ttu-id="5a7c7-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a7c7-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5a7c7-117">-InstanceName</span></span>
<span data-ttu-id="5a7c7-118">인스턴스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="5a7c7-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5a7c7-119">-IntervalSeconds</span></span>
<span data-ttu-id="5a7c7-120">컬렉션 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="5a7c7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a7c7-121">-Name</span></span>
<span data-ttu-id="5a7c7-122">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="5a7c7-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="5a7c7-123">-ObjectName</span></span>
<span data-ttu-id="5a7c7-124">개체의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="5a7c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a7c7-126">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5a7c7-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="5a7c7-127">-UseLegacyCollector</span></span>
<span data-ttu-id="5a7c7-128">레거시 수집기 또는 기본 수집기 사용.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="5a7c7-129">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="5a7c7-129">-Workspace</span></span>
<span data-ttu-id="5a7c7-130">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5a7c7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5a7c7-131">-WorkspaceName</span></span>
<span data-ttu-id="5a7c7-132">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5a7c7-133">-확인</span><span class="sxs-lookup"><span data-stu-id="5a7c7-133">-Confirm</span></span>
<span data-ttu-id="5a7c7-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7c7-135">-WhatIf</span></span>
<span data-ttu-id="5a7c7-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7c7-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7c7-138">CommonParameters</span></span>
<span data-ttu-id="5a7c7-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7c7-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5a7c7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7c7-141">입력</span><span class="sxs-lookup"><span data-stu-id="5a7c7-141">INPUTS</span></span>

### <span data-ttu-id="5a7c7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a7c7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5a7c7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5a7c7-143">System.String</span></span>

### <span data-ttu-id="5a7c7-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5a7c7-144">System.Int32</span></span>

## <span data-ttu-id="5a7c7-145">출력</span><span class="sxs-lookup"><span data-stu-id="5a7c7-145">OUTPUTS</span></span>

### <span data-ttu-id="5a7c7-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5a7c7-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5a7c7-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a7c7-147">NOTES</span></span>

## <span data-ttu-id="5a7c7-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a7c7-148">RELATED LINKS</span></span>
