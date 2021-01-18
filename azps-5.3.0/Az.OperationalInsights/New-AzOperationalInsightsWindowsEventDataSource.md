---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492508"
---
# <span data-ttu-id="fbfae-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="fbfae-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="fbfae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbfae-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfae-103">Windows 운영 체제를 실행한 컴퓨터에서 이벤트 로그를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="fbfae-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbfae-104">SYNTAX</span></span>

### <span data-ttu-id="fbfae-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fbfae-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfae-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fbfae-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbfae-107">설명</span><span class="sxs-lookup"><span data-stu-id="fbfae-107">DESCRIPTION</span></span>
<span data-ttu-id="fbfae-108">**New-AzOperationalInsightsWindowsEventDataSource** cmdlet은 Azure Operational Insights에서 Windows 운영 체제를 실행하는 연결된 컴퓨터에서 Windows 이벤트 로그를 수집하는 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="fbfae-109">예제</span><span class="sxs-lookup"><span data-stu-id="fbfae-109">EXAMPLES</span></span>

### <span data-ttu-id="fbfae-110">예제 1: 시스템 Windows 이벤트 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="fbfae-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="fbfae-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbfae-111">PARAMETERS</span></span>

### <span data-ttu-id="fbfae-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="fbfae-112">-CollectErrors</span></span>
<span data-ttu-id="fbfae-113">Operational Insights가 오류 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="fbfae-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="fbfae-114">-CollectInformation</span></span>
<span data-ttu-id="fbfae-115">Operational Insights가 정보 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="fbfae-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="fbfae-116">-CollectWarnings</span></span>
<span data-ttu-id="fbfae-117">Operational Insights가 경고 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="fbfae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfae-118">-DefaultProfile</span></span>
<span data-ttu-id="fbfae-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fbfae-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbfae-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="fbfae-120">-EventLogName</span></span>
<span data-ttu-id="fbfae-121">이벤트 로그의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="fbfae-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fbfae-122">-Force</span></span>
<span data-ttu-id="fbfae-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fbfae-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fbfae-124">-Name</span></span>
<span data-ttu-id="fbfae-125">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-125">Specifies a name for the data source.</span></span> <span data-ttu-id="fbfae-126">이름은 Azure Portal에서 노출되지 않습니다. 고유하면 문자열을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="fbfae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfae-127">-ResourceGroupName</span></span>
<span data-ttu-id="fbfae-128">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="fbfae-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="fbfae-129">-Workspace</span></span>
<span data-ttu-id="fbfae-130">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fbfae-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbfae-131">-WorkspaceName</span></span>
<span data-ttu-id="fbfae-132">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fbfae-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbfae-133">-Confirm</span></span>
<span data-ttu-id="fbfae-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbfae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbfae-135">-WhatIf</span></span>
<span data-ttu-id="fbfae-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fbfae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbfae-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbfae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfae-138">CommonParameters</span></span>
<span data-ttu-id="fbfae-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbfae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfae-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fbfae-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfae-141">입력</span><span class="sxs-lookup"><span data-stu-id="fbfae-141">INPUTS</span></span>

### <span data-ttu-id="fbfae-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fbfae-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fbfae-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fbfae-143">System.String</span></span>

## <span data-ttu-id="fbfae-144">출력</span><span class="sxs-lookup"><span data-stu-id="fbfae-144">OUTPUTS</span></span>

### <span data-ttu-id="fbfae-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fbfae-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fbfae-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbfae-146">NOTES</span></span>

## <span data-ttu-id="fbfae-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbfae-147">RELATED LINKS</span></span>
