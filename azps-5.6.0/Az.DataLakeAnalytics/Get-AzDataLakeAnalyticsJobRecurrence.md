---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 751fa50a6c29c826fe707852efa661b78d1b9c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004267"
---
# <span data-ttu-id="b9136-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="b9136-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="b9136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9136-102">SYNOPSIS</span></span>
<span data-ttu-id="b9136-103">Data Lake Analytics 작업 재발 또는 재발을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="b9136-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9136-104">SYNTAX</span></span>

### <span data-ttu-id="b9136-105">GetAllInAccount(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9136-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9136-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="b9136-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9136-107">설명</span><span class="sxs-lookup"><span data-stu-id="b9136-107">DESCRIPTION</span></span>
<span data-ttu-id="b9136-108">**Get-AzDataLakeAnalyticsJobRecurrence는** 지정된 Azure Data Lake Analytics 작업 재발 또는 재발 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="b9136-109">예제</span><span class="sxs-lookup"><span data-stu-id="b9136-109">EXAMPLES</span></span>

### <span data-ttu-id="b9136-110">예제 1: 지정된 재발을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="b9136-111">이 명령은 계정 'contosoadla'에서 id '83cb7ad2-3523-4b82-b909-d478b0d8aea3'을 사용하여 지정된 작업 재발을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="b9136-112">예제 2: 계정의 모든 재발 목록 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="b9136-113">이 명령은 계정 "contosoadla"의 모든 재발 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="b9136-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9136-114">PARAMETERS</span></span>

### <span data-ttu-id="b9136-115">-Account</span><span class="sxs-lookup"><span data-stu-id="b9136-115">-Account</span></span>
<span data-ttu-id="b9136-116">작업 되버런스를 검색하려는 Data Lake Analytics 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="b9136-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9136-117">-DefaultProfile</span></span>
<span data-ttu-id="b9136-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b9136-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9136-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="b9136-119">-RecurrenceId</span></span>
<span data-ttu-id="b9136-120">정보를 반환할 특정 작업 되돌리기 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="b9136-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="b9136-121">-SubmittedAfter</span></span>
<span data-ttu-id="b9136-122">지정된 시간 후에만 제출된 작업 되발을 반환하는 선택적 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="b9136-123">-submittedBefore</span><span class="sxs-lookup"><span data-stu-id="b9136-123">-SubmittedBefore</span></span>
<span data-ttu-id="b9136-124">지정된 시간 전에만 제출된 작업 되버런스를 반환하는 선택적 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="b9136-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9136-125">CommonParameters</span></span>
<span data-ttu-id="b9136-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9136-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9136-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9136-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9136-128">입력</span><span class="sxs-lookup"><span data-stu-id="b9136-128">INPUTS</span></span>

### <span data-ttu-id="b9136-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b9136-129">System.String</span></span>

### <span data-ttu-id="b9136-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b9136-130">System.Guid</span></span>

### <span data-ttu-id="b9136-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b9136-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b9136-132">출력</span><span class="sxs-lookup"><span data-stu-id="b9136-132">OUTPUTS</span></span>

### <span data-ttu-id="b9136-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="b9136-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="b9136-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9136-134">NOTES</span></span>

## <span data-ttu-id="b9136-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9136-135">RELATED LINKS</span></span>
