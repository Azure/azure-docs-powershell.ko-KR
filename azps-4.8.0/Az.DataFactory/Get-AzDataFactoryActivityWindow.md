---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212544"
---
# <span data-ttu-id="0174a-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="0174a-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="0174a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0174a-102">SYNOPSIS</span></span>
<span data-ttu-id="0174a-103">Data factory와 연결 된 활동 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="0174a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0174a-104">SYNTAX</span></span>

### <span data-ttu-id="0174a-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0174a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0174a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0174a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0174a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0174a-107">DESCRIPTION</span></span>
<span data-ttu-id="0174a-108">**AzDataFactoryActivityWindow** cmdlet은 data factory에 연결 된 작업 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="0174a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0174a-109">EXAMPLES</span></span>

### <span data-ttu-id="0174a-110">예제 1: 데이터 팩터리에 연결 된 작업 창 가져오기</span><span class="sxs-lookup"><span data-stu-id="0174a-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="0174a-111">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 활동 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="0174a-112">변수</span><span class="sxs-lookup"><span data-stu-id="0174a-112">PARAMETERS</span></span>

### <span data-ttu-id="0174a-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="0174a-113">-ActivityName</span></span>
<span data-ttu-id="0174a-114">활동의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="0174a-115">이 cmdlet은이 매개 변수에서 지정 하는 활동에 대 한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0174a-116">-DataFactory</span></span>
<span data-ttu-id="0174a-117">Cmdlet에서 반환 되는 **PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="0174a-118">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0174a-119">-DataFactoryName</span></span>
<span data-ttu-id="0174a-120">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="0174a-121">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="0174a-122">-DatasetName</span></span>
<span data-ttu-id="0174a-123">데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="0174a-124">이 cmdlet은이 매개 변수에서 지정 하는 데이터 집합에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0174a-125">-DefaultProfile</span></span>
<span data-ttu-id="0174a-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0174a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0174a-127">-필터</span><span class="sxs-lookup"><span data-stu-id="0174a-127">-Filter</span></span>
<span data-ttu-id="0174a-128">Azure 검색 필터 문법을 사용 하 여 표시 되는 활동 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="0174a-129">문법에 대 한 자세한 내용은 MSDN 검색에 대 한 OData Expression 구문을 참조 하세요 https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0174a-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="0174a-130">활동 창 목록은이 매개 변수에서 지정 하는 검색 문자열을 기준으로 필터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="0174a-131">-OrderBy</span></span>
<span data-ttu-id="0174a-132">활동 창 목록 매개 변수 중 하나를 기준으로 응답을 정렬 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="0174a-133">쉼표로 구분 된 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="0174a-134">예: WindowStart, 완료율</span><span class="sxs-lookup"><span data-stu-id="0174a-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="0174a-135">기본적으로 순서는 오름차순 (ASC)입니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="0174a-136">목록의 순서를 내림차순으로 정렬 하려면 DESC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="0174a-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="0174a-137">-PipelineName</span></span>
<span data-ttu-id="0174a-138">파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="0174a-139">이 cmdlet은이 매개 변수에서 지정 하는 파이프라인에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0174a-140">-ResourceGroupName</span></span>
<span data-ttu-id="0174a-141">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="0174a-142">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="0174a-143">-RunEnd</span></span>
<span data-ttu-id="0174a-144">활동 창 실행 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="0174a-145">이 cmdlet은 실행 시간이 *Runstart* 와 *runstart* 사이에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="0174a-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="0174a-146">-RunStart</span></span>
<span data-ttu-id="0174a-147">활동 창 실행의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="0174a-148">이 cmdlet은 실행 시간이 *Runstart* 와 *runstart* 사이에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="0174a-149">-위쪽</span><span class="sxs-lookup"><span data-stu-id="0174a-149">-Top</span></span>
<span data-ttu-id="0174a-150">이 cmdlet이 반환 하는 최대 활동 창 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="0174a-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="0174a-151">-WindowEnd</span></span>
<span data-ttu-id="0174a-152">활동 창의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="0174a-153">이 cmdlet은 *Windowstart* 와 *windowstart* 시간 사이에 시간이 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="0174a-154">WindowStart</span><span class="sxs-lookup"><span data-stu-id="0174a-154">-WindowStart</span></span>
<span data-ttu-id="0174a-155">활동 창의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="0174a-156">이 cmdlet은 *Windowstart* 와 *windowstart* 시간 사이에 시간이 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="0174a-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="0174a-157">-WindowState</span></span>
<span data-ttu-id="0174a-158">활동 창의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="0174a-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0174a-160">않아야</span><span class="sxs-lookup"><span data-stu-id="0174a-160">None</span></span>
- <span data-ttu-id="0174a-161">기다립니다</span><span class="sxs-lookup"><span data-stu-id="0174a-161">Waiting</span></span>
- <span data-ttu-id="0174a-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="0174a-162">InProgress</span></span>
- <span data-ttu-id="0174a-163">수행할</span><span class="sxs-lookup"><span data-stu-id="0174a-163">Ready</span></span>
- <span data-ttu-id="0174a-164">못함</span><span class="sxs-lookup"><span data-stu-id="0174a-164">Failed</span></span>
- <span data-ttu-id="0174a-165">건너뜀이 cmdlet은이 매개 변수에서 지정 하는 상태의 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-166">WindowSubstate 상태의 하위 수준</span><span class="sxs-lookup"><span data-stu-id="0174a-166">-WindowSubstate</span></span>
<span data-ttu-id="0174a-167">활동 창의 하위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="0174a-168">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0174a-169">작업이</span><span class="sxs-lookup"><span data-stu-id="0174a-169">Canceled</span></span>
- <span data-ttu-id="0174a-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="0174a-170">timedOut</span></span>
- <span data-ttu-id="0174a-171">이 cmdlet의 유효성을 검사 하면이 매개 변수에서 지정 하는 하위 상태의 하위 작업 창이 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="0174a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0174a-172">CommonParameters</span></span>
<span data-ttu-id="0174a-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0174a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0174a-174">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0174a-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0174a-175">입력</span><span class="sxs-lookup"><span data-stu-id="0174a-175">INPUTS</span></span>

### <span data-ttu-id="0174a-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0174a-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0174a-177">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0174a-177">System.String</span></span>

### <span data-ttu-id="0174a-178">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0174a-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0174a-179">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="0174a-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0174a-180">출력</span><span class="sxs-lookup"><span data-stu-id="0174a-180">OUTPUTS</span></span>

### <span data-ttu-id="0174a-181">DataFactories. a i m.</span><span class="sxs-lookup"><span data-stu-id="0174a-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="0174a-182">상속자</span><span class="sxs-lookup"><span data-stu-id="0174a-182">NOTES</span></span>

## <span data-ttu-id="0174a-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0174a-183">RELATED LINKS</span></span>

[<span data-ttu-id="0174a-184">Azure Data 팩토리 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0174a-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


