---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056135"
---
# <span data-ttu-id="4cda1-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="4cda1-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="4cda1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cda1-102">SYNOPSIS</span></span>
<span data-ttu-id="4cda1-103">Linux 컴퓨터에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="4cda1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cda1-104">SYNTAX</span></span>

### <span data-ttu-id="4cda1-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cda1-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cda1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4cda1-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cda1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4cda1-107">DESCRIPTION</span></span>
<span data-ttu-id="4cda1-108">**AzOperationalInsightsLinuxSyslogDataSource** cmdlet은 작업 영역의 연결 된 Linux 컴퓨터에 syslog 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="4cda1-109">Azure Operational Insights는 syslog 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="4cda1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4cda1-110">EXAMPLES</span></span>

### <span data-ttu-id="4cda1-111">예제 1: syslog 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="4cda1-111">Example 1: Create syslog data sources</span></span>
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

## <span data-ttu-id="4cda1-112">변수</span><span class="sxs-lookup"><span data-stu-id="4cda1-112">PARAMETERS</span></span>

### <span data-ttu-id="4cda1-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="4cda1-113">-CollectAlert</span></span>
<span data-ttu-id="4cda1-114">Operational Insights가 알림 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="4cda1-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="4cda1-115">-CollectCritical</span></span>
<span data-ttu-id="4cda1-116">Operational Insights에 중요 한 메시지가 수집 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="4cda1-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="4cda1-117">-CollectDebug</span></span>
<span data-ttu-id="4cda1-118">Operational Insights에서 디버그 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="4cda1-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="4cda1-119">-CollectEmergency</span></span>
<span data-ttu-id="4cda1-120">Operational Insights 긴급 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="4cda1-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="4cda1-121">-CollectError</span></span>
<span data-ttu-id="4cda1-122">Operational Insights에서 오류 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="4cda1-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="4cda1-123">-CollectInformational</span></span>
<span data-ttu-id="4cda1-124">Operational Insights가 정보 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="4cda1-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="4cda1-125">-CollectNotice</span></span>
<span data-ttu-id="4cda1-126">Operational Insights에서 알림 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="4cda1-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="4cda1-127">-CollectWarning</span></span>
<span data-ttu-id="4cda1-128">Syslog에 경고 메시지가 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="4cda1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cda1-129">-DefaultProfile</span></span>
<span data-ttu-id="4cda1-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4cda1-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cda1-131">-시설</span><span class="sxs-lookup"><span data-stu-id="4cda1-131">-Facility</span></span>
<span data-ttu-id="4cda1-132">기능 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="4cda1-133">-Force</span><span class="sxs-lookup"><span data-stu-id="4cda1-133">-Force</span></span>
<span data-ttu-id="4cda1-134">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cda1-135">-이름</span><span class="sxs-lookup"><span data-stu-id="4cda1-135">-Name</span></span>
<span data-ttu-id="4cda1-136">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-136">Specifies a name for the data source.</span></span> <span data-ttu-id="4cda1-137">이름이 Azure 포털에는 표시 되지 않으며, 모든 문자열이 고유 하기만 하는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="4cda1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cda1-138">-ResourceGroupName</span></span>
<span data-ttu-id="4cda1-139">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="4cda1-140">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="4cda1-140">-Workspace</span></span>
<span data-ttu-id="4cda1-141">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4cda1-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4cda1-142">-WorkspaceName</span></span>
<span data-ttu-id="4cda1-143">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4cda1-144">-확인</span><span class="sxs-lookup"><span data-stu-id="4cda1-144">-Confirm</span></span>
<span data-ttu-id="4cda1-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cda1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cda1-146">-WhatIf</span></span>
<span data-ttu-id="4cda1-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cda1-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cda1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cda1-149">CommonParameters</span></span>
<span data-ttu-id="4cda1-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cda1-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cda1-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cda1-152">입력</span><span class="sxs-lookup"><span data-stu-id="4cda1-152">INPUTS</span></span>

### <span data-ttu-id="4cda1-153">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="4cda1-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="4cda1-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4cda1-154">System.String</span></span>

## <span data-ttu-id="4cda1-155">출력</span><span class="sxs-lookup"><span data-stu-id="4cda1-155">OUTPUTS</span></span>

### <span data-ttu-id="4cda1-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="4cda1-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="4cda1-157">상속자</span><span class="sxs-lookup"><span data-stu-id="4cda1-157">NOTES</span></span>

## <span data-ttu-id="4cda1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cda1-158">RELATED LINKS</span></span>

[<span data-ttu-id="4cda1-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="4cda1-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="4cda1-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="4cda1-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


