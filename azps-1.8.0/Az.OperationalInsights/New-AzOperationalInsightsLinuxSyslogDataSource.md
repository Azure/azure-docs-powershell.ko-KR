---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699844"
---
# <span data-ttu-id="276ce-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="276ce-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="276ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="276ce-102">SYNOPSIS</span></span>
<span data-ttu-id="276ce-103">Linux 컴퓨터에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="276ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="276ce-104">SYNTAX</span></span>

### <span data-ttu-id="276ce-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="276ce-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="276ce-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="276ce-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="276ce-107">설명은</span><span class="sxs-lookup"><span data-stu-id="276ce-107">DESCRIPTION</span></span>
<span data-ttu-id="276ce-108">**AzOperationalInsightsLinuxSyslogDataSource** cmdlet은 작업 영역의 연결 된 Linux 컴퓨터에 syslog 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="276ce-109">Azure Operational Insights는 syslog 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="276ce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="276ce-110">EXAMPLES</span></span>

## <span data-ttu-id="276ce-111">변수</span><span class="sxs-lookup"><span data-stu-id="276ce-111">PARAMETERS</span></span>

### <span data-ttu-id="276ce-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="276ce-112">-CollectAlert</span></span>
<span data-ttu-id="276ce-113">Operational Insights가 알림 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="276ce-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="276ce-114">-CollectCritical</span></span>
<span data-ttu-id="276ce-115">Operational Insights에 중요 한 메시지가 수집 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="276ce-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="276ce-116">-CollectDebug</span></span>
<span data-ttu-id="276ce-117">Operational Insights에서 디버그 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="276ce-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="276ce-118">-CollectEmergency</span></span>
<span data-ttu-id="276ce-119">Operational Insights 긴급 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="276ce-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="276ce-120">-CollectError</span></span>
<span data-ttu-id="276ce-121">Operational Insights에서 오류 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="276ce-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="276ce-122">-CollectInformational</span></span>
<span data-ttu-id="276ce-123">Operational Insights가 정보 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="276ce-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="276ce-124">-CollectNotice</span></span>
<span data-ttu-id="276ce-125">Operational Insights에서 알림 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="276ce-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="276ce-126">-CollectWarning</span></span>
<span data-ttu-id="276ce-127">Syslog에 경고 메시지가 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="276ce-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276ce-128">-DefaultProfile</span></span>
<span data-ttu-id="276ce-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="276ce-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="276ce-130">-시설</span><span class="sxs-lookup"><span data-stu-id="276ce-130">-Facility</span></span>
<span data-ttu-id="276ce-131">기능 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="276ce-132">-Force</span><span class="sxs-lookup"><span data-stu-id="276ce-132">-Force</span></span>
<span data-ttu-id="276ce-133">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="276ce-134">-이름</span><span class="sxs-lookup"><span data-stu-id="276ce-134">-Name</span></span>
<span data-ttu-id="276ce-135">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="276ce-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="276ce-136">-ResourceGroupName</span></span>
<span data-ttu-id="276ce-137">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="276ce-138">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="276ce-138">-Workspace</span></span>
<span data-ttu-id="276ce-139">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="276ce-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="276ce-140">-WorkspaceName</span></span>
<span data-ttu-id="276ce-141">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="276ce-142">-확인</span><span class="sxs-lookup"><span data-stu-id="276ce-142">-Confirm</span></span>
<span data-ttu-id="276ce-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="276ce-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="276ce-144">-WhatIf</span></span>
<span data-ttu-id="276ce-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="276ce-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="276ce-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276ce-147">CommonParameters</span></span>
<span data-ttu-id="276ce-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="276ce-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276ce-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276ce-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276ce-150">입력</span><span class="sxs-lookup"><span data-stu-id="276ce-150">INPUTS</span></span>

### <span data-ttu-id="276ce-151">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="276ce-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="276ce-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="276ce-152">System.String</span></span>

## <span data-ttu-id="276ce-153">출력</span><span class="sxs-lookup"><span data-stu-id="276ce-153">OUTPUTS</span></span>

### <span data-ttu-id="276ce-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="276ce-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="276ce-155">상속자</span><span class="sxs-lookup"><span data-stu-id="276ce-155">NOTES</span></span>

## <span data-ttu-id="276ce-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="276ce-156">RELATED LINKS</span></span>

[<span data-ttu-id="276ce-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="276ce-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="276ce-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="276ce-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


