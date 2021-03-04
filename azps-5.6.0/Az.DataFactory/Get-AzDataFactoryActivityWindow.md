---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 009f7033b7ecfe26e314a105d0bf88a7433962c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954747"
---
# <span data-ttu-id="c8a8f-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="c8a8f-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="c8a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a8f-103">데이터 팩터리와 연결된 활동 창에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="c8a8f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8a8f-104">SYNTAX</span></span>

### <span data-ttu-id="c8a8f-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c8a8f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8a8f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c8a8f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8a8f-107">설명</span><span class="sxs-lookup"><span data-stu-id="c8a8f-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a8f-108">**Get-AzDataFactoryActivityWindow** cmdlet은 데이터 팩터리와 연결된 활동 창에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="c8a8f-109">예제</span><span class="sxs-lookup"><span data-stu-id="c8a8f-109">EXAMPLES</span></span>

### <span data-ttu-id="c8a8f-110">예제 1: 데이터 팩터리와 연결된 활동 창을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="c8a8f-111">이 명령은 WikiADF라는 데이터 팩터리와 연결된 모든 활동 창에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="c8a8f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8a8f-112">PARAMETERS</span></span>

### <span data-ttu-id="c8a8f-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="c8a8f-113">-ActivityName</span></span>
<span data-ttu-id="c8a8f-114">활동의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="c8a8f-115">이 cmdlet은 이 매개 변수가 지정하는 활동에 대한 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c8a8f-116">-DataFactory</span></span>
<span data-ttu-id="c8a8f-117">cmdlet에서 **반환된 PSDataFactory** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="c8a8f-118">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c8a8f-119">-DataFactoryName</span></span>
<span data-ttu-id="c8a8f-120">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="c8a8f-121">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="c8a8f-122">-DatasetName</span></span>
<span data-ttu-id="c8a8f-123">데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="c8a8f-124">이 cmdlet은 이 매개 변수가 지정하는 데이터 세트에 속하는 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a8f-125">-DefaultProfile</span></span>
<span data-ttu-id="c8a8f-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c8a8f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a8f-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="c8a8f-127">-Filter</span></span>
<span data-ttu-id="c8a8f-128">Azure Search 필터 문법을 사용하여 표현된 활동 창을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="c8a8f-129">문법에 대한 자세한 내용은 AZURE Search용 OData 식 https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) 구문(MSDN)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="c8a8f-130">활동 창 목록은 이 매개 변수가 지정하는 검색 문자열에 의해 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="c8a8f-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c8a8f-131">-OrderBy</span></span>
<span data-ttu-id="c8a8f-132">활동 창 목록 매개 변수 중 하나에 따라 응답을 순서대로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="c8a8f-133">콤마로 구분된 속성의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="c8a8f-134">예: WindowStart, PercentComplete입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="c8a8f-135">기본적으로 순서는 ASC(오차 순서)입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="c8a8f-136">목록을 내선 순서로 주문하려는 경우 DESC를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="c8a8f-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="c8a8f-137">-PipelineName</span></span>
<span data-ttu-id="c8a8f-138">파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="c8a8f-139">이 cmdlet은 이 매개 변수가 지정하는 파이프라인에 속하는 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a8f-140">-ResourceGroupName</span></span>
<span data-ttu-id="c8a8f-141">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c8a8f-142">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹에 속하는 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="c8a8f-143">-RunEnd</span></span>
<span data-ttu-id="c8a8f-144">활동 창 실행의 종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="c8a8f-145">이 cmdlet은 *RunStart와* *RunEnd* 시간 사이에 실행 시간을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="c8a8f-146">-RunStart</span></span>
<span data-ttu-id="c8a8f-147">활동 창 실행의 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="c8a8f-148">이 cmdlet은 *RunStart와* *RunEnd* 시간 사이에 실행 시간을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-149">-Top</span><span class="sxs-lookup"><span data-stu-id="c8a8f-149">-Top</span></span>
<span data-ttu-id="c8a8f-150">이 cmdlet이 반환하는 최대 활동 창 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="c8a8f-151">-WindowEnd</span></span>
<span data-ttu-id="c8a8f-152">활동 기간의 종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="c8a8f-153">이 cmdlet은 *WindowsStart와 WindowEnd* 시간 사이에 있는 활동 *창을* 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="c8a8f-154">-WindowStart</span></span>
<span data-ttu-id="c8a8f-155">활동 창의 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="c8a8f-156">이 cmdlet은 *WindowsStart와 WindowEnd* 시간 사이에 있는 활동 *창을* 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a8f-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="c8a8f-157">-WindowState</span></span>
<span data-ttu-id="c8a8f-158">활동 창의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="c8a8f-159">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8a8f-160">없음</span><span class="sxs-lookup"><span data-stu-id="c8a8f-160">None</span></span>
- <span data-ttu-id="c8a8f-161">대기 중</span><span class="sxs-lookup"><span data-stu-id="c8a8f-161">Waiting</span></span>
- <span data-ttu-id="c8a8f-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="c8a8f-162">InProgress</span></span>
- <span data-ttu-id="c8a8f-163">준비 중</span><span class="sxs-lookup"><span data-stu-id="c8a8f-163">Ready</span></span>
- <span data-ttu-id="c8a8f-164">실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-164">Failed</span></span>
- <span data-ttu-id="c8a8f-165">건너뛴 이 cmdlet은 이 매개 변수가 지정하는 상태의 활동 창을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="c8a8f-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="c8a8f-166">-WindowSubstate</span></span>
<span data-ttu-id="c8a8f-167">활동 창의 하위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="c8a8f-168">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8a8f-169">취소되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-169">Canceled</span></span>
- <span data-ttu-id="c8a8f-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="c8a8f-170">timedOut</span></span>
- <span data-ttu-id="c8a8f-171">이 cmdlet의 유효성을 검사하면 이 매개 변수가 지정하는 하위 하위에 있는 활동 창이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="c8a8f-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a8f-172">CommonParameters</span></span>
<span data-ttu-id="c8a8f-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a8f-174">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8a8f-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a8f-175">입력</span><span class="sxs-lookup"><span data-stu-id="c8a8f-175">INPUTS</span></span>

### <span data-ttu-id="c8a8f-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c8a8f-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c8a8f-177">System.String</span><span class="sxs-lookup"><span data-stu-id="c8a8f-177">System.String</span></span>

### <span data-ttu-id="c8a8f-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8a8f-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8a8f-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8a8f-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c8a8f-180">출력</span><span class="sxs-lookup"><span data-stu-id="c8a8f-180">OUTPUTS</span></span>

### <span data-ttu-id="c8a8f-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="c8a8f-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="c8a8f-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8a8f-182">NOTES</span></span>

## <span data-ttu-id="c8a8f-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8a8f-183">RELATED LINKS</span></span>

[<span data-ttu-id="c8a8f-184">Azure Data Factories Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8a8f-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


