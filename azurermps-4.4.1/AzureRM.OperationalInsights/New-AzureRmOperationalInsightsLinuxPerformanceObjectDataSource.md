---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529227"
---
# <span data-ttu-id="3ecdc-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="3ecdc-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="3ecdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ecdc-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecdc-103">작업 영역의 모든 Linux 컴퓨터에 성능 카운터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ecdc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ecdc-104">SYNTAX</span></span>

### <span data-ttu-id="3ecdc-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ecdc-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ecdc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3ecdc-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ecdc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3ecdc-107">DESCRIPTION</span></span>
<span data-ttu-id="3ecdc-108">**AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** Cmdlet은 Azure Operational Insights가 작업 영역의 모든 Linux 컴퓨터에 데이터를 수집 하는 성능 카운터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3ecdc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3ecdc-109">EXAMPLES</span></span>

## <span data-ttu-id="3ecdc-110">변수</span><span class="sxs-lookup"><span data-stu-id="3ecdc-110">PARAMETERS</span></span>

### <span data-ttu-id="3ecdc-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="3ecdc-111">-CounterNames</span></span>
<span data-ttu-id="3ecdc-112">카운터 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="3ecdc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ecdc-113">-Force</span></span>
<span data-ttu-id="3ecdc-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ecdc-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3ecdc-115">-InstanceName</span></span>
<span data-ttu-id="3ecdc-116">인스턴스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="3ecdc-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="3ecdc-117">-IntervalSeconds</span></span>
<span data-ttu-id="3ecdc-118">수집 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="3ecdc-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3ecdc-119">-Name</span></span>
<span data-ttu-id="3ecdc-120">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3ecdc-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3ecdc-121">-ObjectName</span></span>
<span data-ttu-id="3ecdc-122">개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="3ecdc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecdc-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ecdc-124">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-124">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="3ecdc-125">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="3ecdc-125">-Workspace</span></span>
<span data-ttu-id="3ecdc-126">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ecdc-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ecdc-127">-WorkspaceName</span></span>
<span data-ttu-id="3ecdc-128">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ecdc-129">-확인</span><span class="sxs-lookup"><span data-stu-id="3ecdc-129">-Confirm</span></span>
<span data-ttu-id="3ecdc-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ecdc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ecdc-131">-WhatIf</span></span>
<span data-ttu-id="3ecdc-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ecdc-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ecdc-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecdc-134">-DefaultProfile</span></span>
<span data-ttu-id="3ecdc-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ecdc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecdc-136">CommonParameters</span></span>
<span data-ttu-id="3ecdc-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecdc-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecdc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecdc-139">입력</span><span class="sxs-lookup"><span data-stu-id="3ecdc-139">INPUTS</span></span>

### <span data-ttu-id="3ecdc-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ecdc-140">PSWorkspace</span></span>
<span data-ttu-id="3ecdc-141">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ecdc-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="3ecdc-142">출력</span><span class="sxs-lookup"><span data-stu-id="3ecdc-142">OUTPUTS</span></span>

### <span data-ttu-id="3ecdc-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3ecdc-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3ecdc-144">상속자</span><span class="sxs-lookup"><span data-stu-id="3ecdc-144">NOTES</span></span>

## <span data-ttu-id="3ecdc-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ecdc-145">RELATED LINKS</span></span>

[<span data-ttu-id="3ecdc-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3ecdc-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="3ecdc-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3ecdc-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


