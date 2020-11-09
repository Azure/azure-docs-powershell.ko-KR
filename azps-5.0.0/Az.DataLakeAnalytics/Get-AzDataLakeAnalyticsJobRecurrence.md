---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305831"
---
# <span data-ttu-id="04e02-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="04e02-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="04e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04e02-102">SYNOPSIS</span></span>
<span data-ttu-id="04e02-103">Data Lake Analytics 작업의 되풀이 또는 되풀이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="04e02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04e02-104">SYNTAX</span></span>

### <span data-ttu-id="04e02-105">GetAllInAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="04e02-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04e02-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="04e02-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e02-107">설명은</span><span class="sxs-lookup"><span data-stu-id="04e02-107">DESCRIPTION</span></span>
<span data-ttu-id="04e02-108">**AzDataLakeAnalyticsJobRecurrence** 에서 지정 된 Azure Data Lake Analytics 작업의 되풀이 또는 되풀이 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="04e02-109">예제의</span><span class="sxs-lookup"><span data-stu-id="04e02-109">EXAMPLES</span></span>

### <span data-ttu-id="04e02-110">예제 1: 지정 된 되풀이 가져오기</span><span class="sxs-lookup"><span data-stu-id="04e02-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="04e02-111">이 명령은 ' contosoadla ' 계정에서 id가 ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' 인 지정 된 작업 되풀이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="04e02-112">예제 2: 계정에 있는 모든 되풀이 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="04e02-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="04e02-113">이 명령은 "contosoadla" 계정의 모든 되풀이 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="04e02-114">변수</span><span class="sxs-lookup"><span data-stu-id="04e02-114">PARAMETERS</span></span>

### <span data-ttu-id="04e02-115">-계정</span><span class="sxs-lookup"><span data-stu-id="04e02-115">-Account</span></span>
<span data-ttu-id="04e02-116">작업 되풀이를 검색 하려는 데이터 호수 분석 계정 이름의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="04e02-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e02-117">-DefaultProfile</span></span>
<span data-ttu-id="04e02-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="04e02-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04e02-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="04e02-119">-RecurrenceId</span></span>
<span data-ttu-id="04e02-120">정보를 반환할 대상에 대 한 특정 작업 되풀이의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04e02-121">-다음 시간 후에 submitted</span><span class="sxs-lookup"><span data-stu-id="04e02-121">-SubmittedAfter</span></span>
<span data-ttu-id="04e02-122">지정 된 시간 이후에 제출 되는 작업 되풀이를 반환 하는 선택적 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="04e02-123">-이전에 submitted</span><span class="sxs-lookup"><span data-stu-id="04e02-123">-SubmittedBefore</span></span>
<span data-ttu-id="04e02-124">지정 된 시간 전에 제출 되는 작업 되풀이를 반환 하는 선택적 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="04e02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e02-125">CommonParameters</span></span>
<span data-ttu-id="04e02-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04e02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e02-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e02-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e02-128">입력</span><span class="sxs-lookup"><span data-stu-id="04e02-128">INPUTS</span></span>

### <span data-ttu-id="04e02-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04e02-129">System.String</span></span>

### <span data-ttu-id="04e02-130">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="04e02-130">System.Guid</span></span>

### <span data-ttu-id="04e02-131">시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04e02-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="04e02-132">출력</span><span class="sxs-lookup"><span data-stu-id="04e02-132">OUTPUTS</span></span>

### <span data-ttu-id="04e02-133">DataLakeAnalytics. PSJobRecurrenceInformation/.</span><span class="sxs-lookup"><span data-stu-id="04e02-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="04e02-134">상속자</span><span class="sxs-lookup"><span data-stu-id="04e02-134">NOTES</span></span>

## <span data-ttu-id="04e02-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04e02-135">RELATED LINKS</span></span>
