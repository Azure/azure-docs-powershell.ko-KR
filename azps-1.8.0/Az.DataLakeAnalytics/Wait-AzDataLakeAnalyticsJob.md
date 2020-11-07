---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3d112a39afc522914e31acbc8c5539a45175fd81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868573"
---
# <span data-ttu-id="d5004-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5004-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d5004-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5004-102">SYNOPSIS</span></span>
<span data-ttu-id="d5004-103">작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="d5004-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5004-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5004-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5004-105">DESCRIPTION</span></span>
<span data-ttu-id="d5004-106">**AzDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake Analytics 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="d5004-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5004-107">EXAMPLES</span></span>

### <span data-ttu-id="d5004-108">예제 1: 작업이 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="d5004-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="d5004-109">다음 명령은 지정 된 ID의 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="d5004-110">변수</span><span class="sxs-lookup"><span data-stu-id="d5004-110">PARAMETERS</span></span>

### <span data-ttu-id="d5004-111">-계정</span><span class="sxs-lookup"><span data-stu-id="d5004-111">-Account</span></span>
<span data-ttu-id="d5004-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d5004-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5004-113">-DefaultProfile</span></span>
<span data-ttu-id="d5004-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5004-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5004-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="d5004-115">-JobId</span></span>
<span data-ttu-id="d5004-116">대기할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5004-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5004-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="d5004-118">대기 작업을 종료 하기 전에 대기할 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5004-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5004-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="d5004-120">각 작업 상태를 확인할 때 까지의 경과 시간을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5004-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5004-121">CommonParameters</span></span>
<span data-ttu-id="d5004-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5004-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5004-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5004-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5004-124">입력</span><span class="sxs-lookup"><span data-stu-id="d5004-124">INPUTS</span></span>

### <span data-ttu-id="d5004-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5004-125">System.String</span></span>

### <span data-ttu-id="d5004-126">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="d5004-126">System.Guid</span></span>

### <span data-ttu-id="d5004-127">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="d5004-127">System.Int32</span></span>

## <span data-ttu-id="d5004-128">출력</span><span class="sxs-lookup"><span data-stu-id="d5004-128">OUTPUTS</span></span>

### <span data-ttu-id="d5004-129">DataLake에 대 한 정보를 보려면</span><span class="sxs-lookup"><span data-stu-id="d5004-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="d5004-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d5004-130">NOTES</span></span>

## <span data-ttu-id="d5004-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5004-131">RELATED LINKS</span></span>

[<span data-ttu-id="d5004-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5004-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d5004-133">중지-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5004-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d5004-134">제출-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5004-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


