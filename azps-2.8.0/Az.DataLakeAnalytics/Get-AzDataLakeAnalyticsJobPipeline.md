---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 5b9046e085e7aaba09e9a13fd641f9c8986ccfd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696920"
---
# <span data-ttu-id="59695-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="59695-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="59695-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59695-102">SYNOPSIS</span></span>
<span data-ttu-id="59695-103">Data Lake Analytics 작업 파이프라인이 나 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59695-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="59695-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59695-104">SYNTAX</span></span>

### <span data-ttu-id="59695-105">GetAllInAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="59695-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59695-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="59695-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59695-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59695-107">DESCRIPTION</span></span>
<span data-ttu-id="59695-108">**AzDataLakeAnalyticsJobPipeline** 에서 지정 된 Azure Data Lake Analytics 작업 파이프라인 또는 파이프라인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59695-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="59695-109">예제의</span><span class="sxs-lookup"><span data-stu-id="59695-109">EXAMPLES</span></span>

### <span data-ttu-id="59695-110">예제 1: 지정 된 파이프라인 가져오기</span><span class="sxs-lookup"><span data-stu-id="59695-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="59695-111">이 명령은 ' contosoadla ' 계정에서 id가 ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' 인 지정 된 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59695-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="59695-112">예제 2: 계정에 있는 모든 파이프라인 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="59695-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="59695-113">이 명령은 "contosoadla" 계정의 모든 파이프라인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59695-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="59695-114">변수</span><span class="sxs-lookup"><span data-stu-id="59695-114">PARAMETERS</span></span>

### <span data-ttu-id="59695-115">-계정</span><span class="sxs-lookup"><span data-stu-id="59695-115">-Account</span></span>
<span data-ttu-id="59695-116">작업 파이프라인을 검색 하는 데 사용할 데이터 호수 분석 계정 이름의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59695-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59695-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59695-117">-DefaultProfile</span></span>
<span data-ttu-id="59695-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="59695-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59695-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="59695-119">-PipelineId</span></span>
<span data-ttu-id="59695-120">정보를 반환할 특정 작업 파이프라인의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="59695-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59695-121">-다음 시간 후에 submitted</span><span class="sxs-lookup"><span data-stu-id="59695-121">-SubmittedAfter</span></span>
<span data-ttu-id="59695-122">지정 된 시간 후에만 제출 되는 작업 파이프라인 (들)을 반환 하는 선택적 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="59695-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59695-123">-이전에 submitted</span><span class="sxs-lookup"><span data-stu-id="59695-123">-SubmittedBefore</span></span>
<span data-ttu-id="59695-124">지정 된 시간 이전에 제출할 때만 작업 파이프라인 (들)을 반환 하는 선택적 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="59695-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59695-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59695-125">CommonParameters</span></span>
<span data-ttu-id="59695-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59695-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59695-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59695-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59695-128">입력</span><span class="sxs-lookup"><span data-stu-id="59695-128">INPUTS</span></span>

### <span data-ttu-id="59695-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59695-129">System.String</span></span>

### <span data-ttu-id="59695-130">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="59695-130">System.Guid</span></span>

### <span data-ttu-id="59695-131">시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59695-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="59695-132">출력</span><span class="sxs-lookup"><span data-stu-id="59695-132">OUTPUTS</span></span>

### <span data-ttu-id="59695-133">DataLakeAnalytics. PSJobPipelineInformation/.</span><span class="sxs-lookup"><span data-stu-id="59695-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="59695-134">상속자</span><span class="sxs-lookup"><span data-stu-id="59695-134">NOTES</span></span>

## <span data-ttu-id="59695-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59695-135">RELATED LINKS</span></span>
