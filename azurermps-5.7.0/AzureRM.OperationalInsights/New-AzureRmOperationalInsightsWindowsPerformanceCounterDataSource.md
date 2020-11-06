---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: b827c9d133ff6fc0bb9df0e1e3e25c3eea23916f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527988"
---
# <span data-ttu-id="6262b-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="6262b-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="6262b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6262b-102">SYNOPSIS</span></span>
<span data-ttu-id="6262b-103">Windows 운영 체제를 실행 하는 연결 된 컴퓨터에 대 한 Windows 성능 카운터 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6262b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6262b-104">SYNTAX</span></span>

### <span data-ttu-id="6262b-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6262b-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6262b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6262b-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6262b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6262b-107">DESCRIPTION</span></span>
<span data-ttu-id="6262b-108">**AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** Cmdlet은 windows 운영 체제를 실행 하는 연결 된 컴퓨터에 대 한 windows 성능 카운터 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="6262b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6262b-109">EXAMPLES</span></span>

## <span data-ttu-id="6262b-110">변수</span><span class="sxs-lookup"><span data-stu-id="6262b-110">PARAMETERS</span></span>

### <span data-ttu-id="6262b-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="6262b-111">-CounterName</span></span>
<span data-ttu-id="6262b-112">카운터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-112">Specifies the name of a counter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6262b-113">-DefaultProfile</span></span>
<span data-ttu-id="6262b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6262b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6262b-115">-Force</span></span>
<span data-ttu-id="6262b-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6262b-117">-InstanceName</span></span>
<span data-ttu-id="6262b-118">인스턴스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="6262b-119">-IntervalSeconds</span></span>
<span data-ttu-id="6262b-120">수집 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6262b-121">-Name</span></span>
<span data-ttu-id="6262b-122">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="6262b-123">-ObjectName</span></span>
<span data-ttu-id="6262b-124">개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6262b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6262b-126">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="6262b-127">-UseLegacyCollector</span></span>
<span data-ttu-id="6262b-128">레거시 수집기 또는 기본 컬렉터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-128">Use legacy collector or the default collector.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-129">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="6262b-129">-Workspace</span></span>
<span data-ttu-id="6262b-130">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6262b-131">-WorkspaceName</span></span>
<span data-ttu-id="6262b-132">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-133">-확인</span><span class="sxs-lookup"><span data-stu-id="6262b-133">-Confirm</span></span>
<span data-ttu-id="6262b-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6262b-135">-WhatIf</span></span>
<span data-ttu-id="6262b-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6262b-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6262b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6262b-138">CommonParameters</span></span>
<span data-ttu-id="6262b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6262b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6262b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6262b-141">입력</span><span class="sxs-lookup"><span data-stu-id="6262b-141">INPUTS</span></span>

### <span data-ttu-id="6262b-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6262b-142">PSWorkspace</span></span>
<span data-ttu-id="6262b-143">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6262b-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="6262b-144">출력</span><span class="sxs-lookup"><span data-stu-id="6262b-144">OUTPUTS</span></span>

### <span data-ttu-id="6262b-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6262b-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6262b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="6262b-146">NOTES</span></span>

## <span data-ttu-id="6262b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6262b-147">RELATED LINKS</span></span>

