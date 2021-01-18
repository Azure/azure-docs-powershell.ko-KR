---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496339"
---
# <span data-ttu-id="59e46-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="59e46-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="59e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59e46-102">SYNOPSIS</span></span>
<span data-ttu-id="59e46-103">Linux 컴퓨터에 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="59e46-104">구문</span><span class="sxs-lookup"><span data-stu-id="59e46-104">SYNTAX</span></span>

### <span data-ttu-id="59e46-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="59e46-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59e46-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="59e46-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59e46-107">설명</span><span class="sxs-lookup"><span data-stu-id="59e46-107">DESCRIPTION</span></span>
<span data-ttu-id="59e46-108">**New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet은 작업 영역의 연결된 Linux 컴퓨터에 syslog 데이터 원본을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="59e46-109">Azure Operational Insights는 syslog 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="59e46-110">예제</span><span class="sxs-lookup"><span data-stu-id="59e46-110">EXAMPLES</span></span>

### <span data-ttu-id="59e46-111">예제 1: syslog 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="59e46-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="59e46-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59e46-112">PARAMETERS</span></span>

### <span data-ttu-id="59e46-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="59e46-113">-CollectAlert</span></span>
<span data-ttu-id="59e46-114">Operational Insights가 경고 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="59e46-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="59e46-115">-CollectCritical</span></span>
<span data-ttu-id="59e46-116">Operational Insights가 중요한 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="59e46-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="59e46-117">-CollectDebug</span></span>
<span data-ttu-id="59e46-118">Operational Insights가 디버그 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="59e46-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="59e46-119">-CollectEmergency</span></span>
<span data-ttu-id="59e46-120">Operational Insights가 긴급 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="59e46-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="59e46-121">-CollectError</span></span>
<span data-ttu-id="59e46-122">Operational Insights가 오류 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="59e46-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="59e46-123">-CollectInformational</span></span>
<span data-ttu-id="59e46-124">Operational Insights가 정보 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="59e46-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="59e46-125">-CollectNotice</span></span>
<span data-ttu-id="59e46-126">Operational Insights가 알림 메시지를 수집하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="59e46-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="59e46-127">-CollectWarning</span></span>
<span data-ttu-id="59e46-128">syslog에 경고 메시지가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="59e46-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e46-129">-DefaultProfile</span></span>
<span data-ttu-id="59e46-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="59e46-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59e46-131">-Facility</span><span class="sxs-lookup"><span data-stu-id="59e46-131">-Facility</span></span>
<span data-ttu-id="59e46-132">시설 코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="59e46-133">-Force</span><span class="sxs-lookup"><span data-stu-id="59e46-133">-Force</span></span>
<span data-ttu-id="59e46-134">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59e46-135">-Name</span><span class="sxs-lookup"><span data-stu-id="59e46-135">-Name</span></span>
<span data-ttu-id="59e46-136">데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-136">Specifies a name for the data source.</span></span> <span data-ttu-id="59e46-137">이름은 Azure Portal에서 노출되지 않습니다. 고유하면 문자열을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="59e46-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e46-138">-ResourceGroupName</span></span>
<span data-ttu-id="59e46-139">Linux 컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="59e46-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="59e46-140">-Workspace</span></span>
<span data-ttu-id="59e46-141">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="59e46-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59e46-142">-WorkspaceName</span></span>
<span data-ttu-id="59e46-143">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="59e46-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59e46-144">-Confirm</span></span>
<span data-ttu-id="59e46-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59e46-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59e46-146">-WhatIf</span></span>
<span data-ttu-id="59e46-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59e46-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59e46-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59e46-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e46-149">CommonParameters</span></span>
<span data-ttu-id="59e46-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59e46-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e46-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59e46-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e46-152">입력</span><span class="sxs-lookup"><span data-stu-id="59e46-152">INPUTS</span></span>

### <span data-ttu-id="59e46-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="59e46-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="59e46-154">System.String</span><span class="sxs-lookup"><span data-stu-id="59e46-154">System.String</span></span>

## <span data-ttu-id="59e46-155">출력</span><span class="sxs-lookup"><span data-stu-id="59e46-155">OUTPUTS</span></span>

### <span data-ttu-id="59e46-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="59e46-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="59e46-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59e46-157">NOTES</span></span>

## <span data-ttu-id="59e46-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59e46-158">RELATED LINKS</span></span>

[<span data-ttu-id="59e46-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="59e46-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="59e46-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="59e46-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


