---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 6372abc324601761c07ec4c69d52db188172ba0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872433"
---
# <span data-ttu-id="3a5af-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="3a5af-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="3a5af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a5af-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5af-103">작업 영역의 모든 Linux 컴퓨터에 성능 카운터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3a5af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a5af-104">SYNTAX</span></span>

### <span data-ttu-id="3a5af-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a5af-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a5af-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a5af-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a5af-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3a5af-107">DESCRIPTION</span></span>
<span data-ttu-id="3a5af-108">**AzOperationalInsightsLinuxPerformanceObjectDataSource** Cmdlet은 Azure Operational Insights가 작업 영역의 모든 Linux 컴퓨터에 데이터를 수집 하는 성능 카운터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3a5af-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3a5af-109">EXAMPLES</span></span>

## <span data-ttu-id="3a5af-110">변수</span><span class="sxs-lookup"><span data-stu-id="3a5af-110">PARAMETERS</span></span>

### <span data-ttu-id="3a5af-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="3a5af-111">-CounterNames</span></span>
<span data-ttu-id="3a5af-112">카운터 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="3a5af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5af-113">-DefaultProfile</span></span>
<span data-ttu-id="3a5af-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a5af-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a5af-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3a5af-115">-Force</span></span>
<span data-ttu-id="3a5af-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a5af-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3a5af-117">-InstanceName</span></span>
<span data-ttu-id="3a5af-118">인스턴스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="3a5af-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="3a5af-119">-IntervalSeconds</span></span>
<span data-ttu-id="3a5af-120">수집 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="3a5af-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3a5af-121">-Name</span></span>
<span data-ttu-id="3a5af-122">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3a5af-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3a5af-123">-ObjectName</span></span>
<span data-ttu-id="3a5af-124">개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="3a5af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a5af-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a5af-126">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="3a5af-127">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="3a5af-127">-Workspace</span></span>
<span data-ttu-id="3a5af-128">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3a5af-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a5af-129">-WorkspaceName</span></span>
<span data-ttu-id="3a5af-130">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3a5af-131">-확인</span><span class="sxs-lookup"><span data-stu-id="3a5af-131">-Confirm</span></span>
<span data-ttu-id="3a5af-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a5af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a5af-133">-WhatIf</span></span>
<span data-ttu-id="3a5af-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a5af-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a5af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5af-136">CommonParameters</span></span>
<span data-ttu-id="3a5af-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5af-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5af-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5af-139">입력</span><span class="sxs-lookup"><span data-stu-id="3a5af-139">INPUTS</span></span>

### <span data-ttu-id="3a5af-140">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="3a5af-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3a5af-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a5af-141">System.String</span></span>

### <span data-ttu-id="3a5af-142">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="3a5af-142">System.String[]</span></span>

### <span data-ttu-id="3a5af-143">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="3a5af-143">System.Int32</span></span>

## <span data-ttu-id="3a5af-144">출력</span><span class="sxs-lookup"><span data-stu-id="3a5af-144">OUTPUTS</span></span>

### <span data-ttu-id="3a5af-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3a5af-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3a5af-146">상속자</span><span class="sxs-lookup"><span data-stu-id="3a5af-146">NOTES</span></span>

## <span data-ttu-id="3a5af-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a5af-147">RELATED LINKS</span></span>

[<span data-ttu-id="3a5af-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3a5af-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="3a5af-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3a5af-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


