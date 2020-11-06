---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 33deeafce23267d1b2dbc594251bc58de1914280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525207"
---
# <span data-ttu-id="276c6-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="276c6-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="276c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="276c6-102">SYNOPSIS</span></span>
<span data-ttu-id="276c6-103">Data factory와 연결 된 활동 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="276c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="276c6-104">SYNTAX</span></span>

### <span data-ttu-id="276c6-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="276c6-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276c6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="276c6-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="276c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="276c6-107">DESCRIPTION</span></span>
<span data-ttu-id="276c6-108">**AzureRmDataFactoryActivityWindow** cmdlet은 data factory에 연결 된 작업 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="276c6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="276c6-109">EXAMPLES</span></span>

### <span data-ttu-id="276c6-110">예제 1: 데이터 팩터리에 연결 된 작업 창 가져오기</span><span class="sxs-lookup"><span data-stu-id="276c6-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="276c6-111">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 활동 창에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="276c6-112">변수</span><span class="sxs-lookup"><span data-stu-id="276c6-112">PARAMETERS</span></span>

### <span data-ttu-id="276c6-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="276c6-113">-ActivityName</span></span>
<span data-ttu-id="276c6-114">활동의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="276c6-115">이 cmdlet은이 매개 변수에서 지정 하는 활동에 대 한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="276c6-116">-DataFactory</span></span>
<span data-ttu-id="276c6-117">Cmdlet에서 반환 되는 **PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="276c6-118">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="276c6-119">-DataFactoryName</span></span>
<span data-ttu-id="276c6-120">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="276c6-121">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="276c6-122">-DatasetName</span></span>
<span data-ttu-id="276c6-123">데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="276c6-124">이 cmdlet은이 매개 변수에서 지정 하는 데이터 집합에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276c6-125">-DefaultProfile</span></span>
<span data-ttu-id="276c6-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="276c6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="276c6-127">-필터</span><span class="sxs-lookup"><span data-stu-id="276c6-127">-Filter</span></span>
<span data-ttu-id="276c6-128">Azure 검색 필터 문법을 사용 하 여 표시 되는 활동 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="276c6-129">문법에 대 한 자세한 내용은 MSDN 검색에 대 한 OData Expression 구문을 참조 하세요 https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) .</span><span class="sxs-lookup"><span data-stu-id="276c6-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="276c6-130">활동 창 목록은이 매개 변수에서 지정 하는 검색 문자열을 기준으로 필터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="276c6-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="276c6-131">-OrderBy</span></span>
<span data-ttu-id="276c6-132">활동 창 목록 매개 변수 중 하나를 기준으로 응답을 정렬 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="276c6-133">쉼표로 구분 된 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="276c6-134">예: WindowStart, 완료율</span><span class="sxs-lookup"><span data-stu-id="276c6-134">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="276c6-135">기본적으로 순서는 오름차순 (ASC)입니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="276c6-136">목록의 순서를 내림차순으로 정렬 하려면 DESC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="276c6-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="276c6-137">-PipelineName</span></span>
<span data-ttu-id="276c6-138">파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="276c6-139">이 cmdlet은이 매개 변수에서 지정 하는 파이프라인에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="276c6-140">-ResourceGroupName</span></span>
<span data-ttu-id="276c6-141">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="276c6-142">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="276c6-143">-RunEnd</span></span>
<span data-ttu-id="276c6-144">활동 창 실행 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="276c6-145">이 cmdlet은 실행 시간이 *Runstart* 와 *runstart* 사이에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="276c6-146">-RunStart</span></span>
<span data-ttu-id="276c6-147">활동 창 실행의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="276c6-148">이 cmdlet은 실행 시간이 *Runstart* 와 *runstart* 사이에 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-149">-위쪽</span><span class="sxs-lookup"><span data-stu-id="276c6-149">-Top</span></span>
<span data-ttu-id="276c6-150">이 cmdlet이 반환 하는 최대 활동 창 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="276c6-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="276c6-151">-WindowEnd</span></span>
<span data-ttu-id="276c6-152">활동 창의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="276c6-153">이 cmdlet은 *Windowstart* 와 *windowstart* 시간 사이에 시간이 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-154">WindowStart</span><span class="sxs-lookup"><span data-stu-id="276c6-154">-WindowStart</span></span>
<span data-ttu-id="276c6-155">활동 창의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="276c6-156">이 cmdlet은 *Windowstart* 와 *windowstart* 시간 사이에 시간이 속하는 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276c6-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="276c6-157">-WindowState</span></span>
<span data-ttu-id="276c6-158">활동 창의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="276c6-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="276c6-160">않아야</span><span class="sxs-lookup"><span data-stu-id="276c6-160">None</span></span>
- <span data-ttu-id="276c6-161">기다립니다</span><span class="sxs-lookup"><span data-stu-id="276c6-161">Waiting</span></span>
- <span data-ttu-id="276c6-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="276c6-162">InProgress</span></span>
- <span data-ttu-id="276c6-163">수행할</span><span class="sxs-lookup"><span data-stu-id="276c6-163">Ready</span></span>
- <span data-ttu-id="276c6-164">못함</span><span class="sxs-lookup"><span data-stu-id="276c6-164">Failed</span></span>
- <span data-ttu-id="276c6-165">건너뛰면</span><span class="sxs-lookup"><span data-stu-id="276c6-165">Skipped</span></span>

<span data-ttu-id="276c6-166">이 cmdlet은이 매개 변수에서 지정 하는 상태의 활동 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-166">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="276c6-167">WindowSubstate 상태의 하위 수준</span><span class="sxs-lookup"><span data-stu-id="276c6-167">-WindowSubstate</span></span>
<span data-ttu-id="276c6-168">활동 창의 하위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-168">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="276c6-169">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="276c6-170">작업이</span><span class="sxs-lookup"><span data-stu-id="276c6-170">Canceled</span></span>
- <span data-ttu-id="276c6-171">timedOut</span><span class="sxs-lookup"><span data-stu-id="276c6-171">timedOut</span></span>
- <span data-ttu-id="276c6-172">을</span><span class="sxs-lookup"><span data-stu-id="276c6-172">Validating</span></span>

<span data-ttu-id="276c6-173">이 cmdlet은이 매개 변수에서 지정 하는 하위 상태의 하위 작업 창을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-173">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="276c6-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276c6-174">CommonParameters</span></span>
<span data-ttu-id="276c6-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276c6-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276c6-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276c6-177">입력</span><span class="sxs-lookup"><span data-stu-id="276c6-177">INPUTS</span></span>

### <span data-ttu-id="276c6-178">않아야</span><span class="sxs-lookup"><span data-stu-id="276c6-178">None</span></span>
<span data-ttu-id="276c6-179">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="276c6-180">출력</span><span class="sxs-lookup"><span data-stu-id="276c6-180">OUTPUTS</span></span>

### <span data-ttu-id="276c6-181">WindowsAzure ' 1 [[]. 유틸리티, WindowsAzure, 유틸리티, Version = 0.8.2.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]을 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="276c6-181">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="276c6-182">상속자</span><span class="sxs-lookup"><span data-stu-id="276c6-182">NOTES</span></span>

## <span data-ttu-id="276c6-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="276c6-183">RELATED LINKS</span></span>

[<span data-ttu-id="276c6-184">Azure Data 팩토리 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="276c6-184">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


