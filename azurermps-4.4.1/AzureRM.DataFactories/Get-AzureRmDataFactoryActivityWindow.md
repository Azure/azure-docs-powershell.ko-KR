---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702230"
---
# <span data-ttu-id="5f36f-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="5f36f-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="5f36f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f36f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f36f-103">Data factory와 연결 된 활동 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f36f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f36f-104">SYNTAX</span></span>

### <span data-ttu-id="5f36f-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f36f-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f36f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5f36f-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f36f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f36f-107">DESCRIPTION</span></span>
<span data-ttu-id="5f36f-108">**AzureRmDataFactoryActivityWindow** cmdlet은 data factory에 연결 된 작업 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="5f36f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5f36f-109">EXAMPLES</span></span>

### <span data-ttu-id="5f36f-110">예제 1: 데이터 팩터리에 연결 된 작업 창 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f36f-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="5f36f-111">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 활동 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="5f36f-112">변수</span><span class="sxs-lookup"><span data-stu-id="5f36f-112">PARAMETERS</span></span>

### <span data-ttu-id="5f36f-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="5f36f-113">-ActivityName</span></span>
<span data-ttu-id="5f36f-114">활동의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="5f36f-115">이 cmdlet은이 매개 변수에서 지정 하는 활동에 대 한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5f36f-116">-DataFactory</span></span>
<span data-ttu-id="5f36f-117">Cmdlet에서 반환 되는 **PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="5f36f-118">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f36f-119">-DataFactoryName</span></span>
<span data-ttu-id="5f36f-120">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="5f36f-121">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="5f36f-122">-DatasetName</span></span>
<span data-ttu-id="5f36f-123">데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="5f36f-124">이 cmdlet은이 매개 변수에서 지정 하는 데이터 집합에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-125">-필터</span><span class="sxs-lookup"><span data-stu-id="5f36f-125">-Filter</span></span>
<span data-ttu-id="5f36f-126">Azure 검색 필터 문법을 사용 하 여 표시 되는 활동 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="5f36f-127">문법에 대 한 자세한 내용은 MSDN 검색에 대 한 OData Expression 구문을 참조 하세요 https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5f36f-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="5f36f-128">활동 창 목록은이 매개 변수에서 지정 하는 검색 문자열을 기준으로 필터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5f36f-129">-OrderBy</span></span>
<span data-ttu-id="5f36f-130">활동 창 목록 매개 변수 중 하나를 기준으로 응답을 정렬 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="5f36f-131">쉼표로 구분 된 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="5f36f-132">예: WindowStart, 완료율</span><span class="sxs-lookup"><span data-stu-id="5f36f-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="5f36f-133">기본적으로 순서는 오름차순 (ASC)입니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="5f36f-134">목록의 순서를 내림차순으로 정렬 하려면 DESC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-134">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="5f36f-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="5f36f-135">-PipelineName</span></span>
<span data-ttu-id="5f36f-136">파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="5f36f-137">이 cmdlet은이 매개 변수에서 지정 하는 파이프라인에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f36f-138">-ResourceGroupName</span></span>
<span data-ttu-id="5f36f-139">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="5f36f-140">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="5f36f-141">-RunEnd</span></span>
<span data-ttu-id="5f36f-142">활동 창 실행 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="5f36f-143">이 cmdlet은 실행 시간이 *Runstart* 와 *runstart* 사이에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="5f36f-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="5f36f-144">-RunStart</span></span>
<span data-ttu-id="5f36f-145">활동 창 실행의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="5f36f-146">이 cmdlet은 실행 시간이 *Runstart* 와 *runstart* 사이에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="5f36f-147">-위쪽</span><span class="sxs-lookup"><span data-stu-id="5f36f-147">-Top</span></span>
<span data-ttu-id="5f36f-148">이 cmdlet이 반환 하는 최대 활동 창 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="5f36f-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="5f36f-149">-WindowEnd</span></span>
<span data-ttu-id="5f36f-150">활동 창의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="5f36f-151">이 cmdlet은 *Windowstart* 와 *windowstart* 시간 사이에 시간이 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="5f36f-152">WindowStart</span><span class="sxs-lookup"><span data-stu-id="5f36f-152">-WindowStart</span></span>
<span data-ttu-id="5f36f-153">활동 창의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="5f36f-154">이 cmdlet은 *Windowstart* 와 *windowstart* 시간 사이에 시간이 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="5f36f-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="5f36f-155">-WindowState</span></span>
<span data-ttu-id="5f36f-156">활동 창의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="5f36f-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f36f-158">않아야</span><span class="sxs-lookup"><span data-stu-id="5f36f-158">None</span></span>
- <span data-ttu-id="5f36f-159">기다립니다</span><span class="sxs-lookup"><span data-stu-id="5f36f-159">Waiting</span></span>
- <span data-ttu-id="5f36f-160">InProgress</span><span class="sxs-lookup"><span data-stu-id="5f36f-160">InProgress</span></span>
- <span data-ttu-id="5f36f-161">수행할</span><span class="sxs-lookup"><span data-stu-id="5f36f-161">Ready</span></span>
- <span data-ttu-id="5f36f-162">못함</span><span class="sxs-lookup"><span data-stu-id="5f36f-162">Failed</span></span>
- <span data-ttu-id="5f36f-163">건너뛰면</span><span class="sxs-lookup"><span data-stu-id="5f36f-163">Skipped</span></span>

<span data-ttu-id="5f36f-164">이 cmdlet은이 매개 변수에서 지정 하는 상태의 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-165">WindowSubstate 상태의 하위 수준</span><span class="sxs-lookup"><span data-stu-id="5f36f-165">-WindowSubstate</span></span>
<span data-ttu-id="5f36f-166">활동 창의 하위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="5f36f-167">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f36f-168">작업이</span><span class="sxs-lookup"><span data-stu-id="5f36f-168">Canceled</span></span>
- <span data-ttu-id="5f36f-169">timedOut</span><span class="sxs-lookup"><span data-stu-id="5f36f-169">timedOut</span></span>
- <span data-ttu-id="5f36f-170">을</span><span class="sxs-lookup"><span data-stu-id="5f36f-170">Validating</span></span>

<span data-ttu-id="5f36f-171">이 cmdlet은이 매개 변수에서 지정 하는 하위 상태의 하위 작업 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f36f-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f36f-172">-DefaultProfile</span></span>
<span data-ttu-id="5f36f-173">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f36f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f36f-174">CommonParameters</span></span>
<span data-ttu-id="5f36f-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f36f-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f36f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f36f-177">입력</span><span class="sxs-lookup"><span data-stu-id="5f36f-177">INPUTS</span></span>

## <span data-ttu-id="5f36f-178">출력</span><span class="sxs-lookup"><span data-stu-id="5f36f-178">OUTPUTS</span></span>

### <span data-ttu-id="5f36f-179">WindowsAzure ' 1 [[]. 유틸리티, WindowsAzure, 유틸리티, Version = 0.8.2.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]을 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f36f-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5f36f-180">상속자</span><span class="sxs-lookup"><span data-stu-id="5f36f-180">NOTES</span></span>

## <span data-ttu-id="5f36f-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f36f-181">RELATED LINKS</span></span>

[<span data-ttu-id="5f36f-182">Azure Data 팩토리 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5f36f-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


