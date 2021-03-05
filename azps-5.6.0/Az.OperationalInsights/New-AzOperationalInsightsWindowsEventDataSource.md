---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 29f109e0e4f063a72e188a908da8bc65723f5065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989893"
---
# <span data-ttu-id="563d0-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="563d0-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="563d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="563d0-102">SYNOPSIS</span></span>
<span data-ttu-id="563d0-103">Windows 운영 체제를 실행하는 컴퓨터에서 이벤트 로그를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="563d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="563d0-104">SYNTAX</span></span>

### <span data-ttu-id="563d0-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="563d0-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="563d0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="563d0-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="563d0-107">설명</span><span class="sxs-lookup"><span data-stu-id="563d0-107">DESCRIPTION</span></span>
<span data-ttu-id="563d0-108">**New-AzOperationalInsightsWindowsEventDataSource** cmdlet은 Azure Operational Insights에서 Windows 운영 체제를 실행하는 연결된 컴퓨터에서 Windows 이벤트 로그를 수집하는 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="563d0-109">예제</span><span class="sxs-lookup"><span data-stu-id="563d0-109">EXAMPLES</span></span>

### <span data-ttu-id="563d0-110">예제 1: 시스템 Windows 이벤트 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="563d0-110">Example 1: Create system Windows event data source</span></span>
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

## <span data-ttu-id="563d0-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="563d0-111">PARAMETERS</span></span>

### <span data-ttu-id="563d0-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="563d0-112">-CollectErrors</span></span>
<span data-ttu-id="563d0-113">Operational Insights가 오류 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="563d0-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="563d0-114">-CollectInformation</span></span>
<span data-ttu-id="563d0-115">Operational Insights가 정보 메시지를 수집하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="563d0-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="563d0-116">-CollectWarnings</span></span>
<span data-ttu-id="563d0-117">Operational Insights가 경고 메시지를 수집하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="563d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563d0-118">-DefaultProfile</span></span>
<span data-ttu-id="563d0-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="563d0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="563d0-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="563d0-120">-EventLogName</span></span>
<span data-ttu-id="563d0-121">이벤트 로그의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="563d0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="563d0-122">-Force</span></span>
<span data-ttu-id="563d0-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="563d0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="563d0-124">-Name</span></span>
<span data-ttu-id="563d0-125">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-125">Specifies a name for the data source.</span></span> <span data-ttu-id="563d0-126">이름은 Azure Portal에 노출되지 않습니다. 고유하면 문자열을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="563d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="563d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="563d0-128">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="563d0-129">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="563d0-129">-Workspace</span></span>
<span data-ttu-id="563d0-130">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="563d0-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="563d0-131">-WorkspaceName</span></span>
<span data-ttu-id="563d0-132">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="563d0-133">-확인</span><span class="sxs-lookup"><span data-stu-id="563d0-133">-Confirm</span></span>
<span data-ttu-id="563d0-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="563d0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="563d0-135">-WhatIf</span></span>
<span data-ttu-id="563d0-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="563d0-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="563d0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563d0-138">CommonParameters</span></span>
<span data-ttu-id="563d0-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="563d0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563d0-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="563d0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563d0-141">입력</span><span class="sxs-lookup"><span data-stu-id="563d0-141">INPUTS</span></span>

### <span data-ttu-id="563d0-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="563d0-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="563d0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="563d0-143">System.String</span></span>

## <span data-ttu-id="563d0-144">출력</span><span class="sxs-lookup"><span data-stu-id="563d0-144">OUTPUTS</span></span>

### <span data-ttu-id="563d0-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="563d0-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="563d0-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="563d0-146">NOTES</span></span>

## <span data-ttu-id="563d0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="563d0-147">RELATED LINKS</span></span>
