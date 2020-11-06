---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 86bc4b8bedbaafb6da1267d94ffa01b3d0ca95c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528467"
---
# <span data-ttu-id="65367-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="65367-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="65367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65367-102">SYNOPSIS</span></span>
<span data-ttu-id="65367-103">Linux 컴퓨터에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65367-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65367-104">SYNTAX</span></span>

### <span data-ttu-id="65367-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="65367-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65367-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="65367-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65367-107">설명은</span><span class="sxs-lookup"><span data-stu-id="65367-107">DESCRIPTION</span></span>
<span data-ttu-id="65367-108">**AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet은 작업 영역의 연결 된 Linux 컴퓨터에 syslog 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="65367-109">Azure Operational Insights는 syslog 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65367-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="65367-110">예제의</span><span class="sxs-lookup"><span data-stu-id="65367-110">EXAMPLES</span></span>

## <span data-ttu-id="65367-111">변수</span><span class="sxs-lookup"><span data-stu-id="65367-111">PARAMETERS</span></span>

### <span data-ttu-id="65367-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="65367-112">-CollectAlert</span></span>
<span data-ttu-id="65367-113">Operational Insights가 알림 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="65367-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="65367-114">-CollectCritical</span></span>
<span data-ttu-id="65367-115">Operational Insights에 중요 한 메시지가 수집 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="65367-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="65367-116">-CollectDebug</span></span>
<span data-ttu-id="65367-117">Operational Insights에서 디버그 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="65367-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="65367-118">-CollectEmergency</span></span>
<span data-ttu-id="65367-119">Operational Insights 긴급 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="65367-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="65367-120">-CollectError</span></span>
<span data-ttu-id="65367-121">Operational Insights에서 오류 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="65367-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="65367-122">-CollectInformational</span></span>
<span data-ttu-id="65367-123">Operational Insights가 정보 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="65367-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="65367-124">-CollectNotice</span></span>
<span data-ttu-id="65367-125">Operational Insights에서 알림 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="65367-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="65367-126">-CollectWarning</span></span>
<span data-ttu-id="65367-127">Syslog에 경고 메시지가 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65367-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="65367-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65367-128">-DefaultProfile</span></span>
<span data-ttu-id="65367-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65367-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65367-130">-시설</span><span class="sxs-lookup"><span data-stu-id="65367-130">-Facility</span></span>
<span data-ttu-id="65367-131">기능 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="65367-132">-Force</span><span class="sxs-lookup"><span data-stu-id="65367-132">-Force</span></span>
<span data-ttu-id="65367-133">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65367-134">-이름</span><span class="sxs-lookup"><span data-stu-id="65367-134">-Name</span></span>
<span data-ttu-id="65367-135">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="65367-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65367-136">-ResourceGroupName</span></span>
<span data-ttu-id="65367-137">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="65367-138">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="65367-138">-Workspace</span></span>
<span data-ttu-id="65367-139">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="65367-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65367-140">-WorkspaceName</span></span>
<span data-ttu-id="65367-141">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="65367-142">-확인</span><span class="sxs-lookup"><span data-stu-id="65367-142">-Confirm</span></span>
<span data-ttu-id="65367-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65367-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65367-144">-WhatIf</span></span>
<span data-ttu-id="65367-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65367-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65367-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65367-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65367-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65367-147">CommonParameters</span></span>
<span data-ttu-id="65367-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65367-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65367-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65367-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65367-150">입력</span><span class="sxs-lookup"><span data-stu-id="65367-150">INPUTS</span></span>

### <span data-ttu-id="65367-151">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="65367-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="65367-152">매개 변수: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65367-152">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="65367-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65367-153">System.String</span></span>

## <span data-ttu-id="65367-154">출력</span><span class="sxs-lookup"><span data-stu-id="65367-154">OUTPUTS</span></span>

### <span data-ttu-id="65367-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="65367-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="65367-156">상속자</span><span class="sxs-lookup"><span data-stu-id="65367-156">NOTES</span></span>

## <span data-ttu-id="65367-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65367-157">RELATED LINKS</span></span>

[<span data-ttu-id="65367-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="65367-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="65367-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="65367-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


