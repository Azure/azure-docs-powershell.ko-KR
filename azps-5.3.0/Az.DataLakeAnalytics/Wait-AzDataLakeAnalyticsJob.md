---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493470"
---
# <span data-ttu-id="69f44-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="69f44-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="69f44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f44-102">SYNOPSIS</span></span>
<span data-ttu-id="69f44-103">작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="69f44-104">구문</span><span class="sxs-lookup"><span data-stu-id="69f44-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f44-105">설명</span><span class="sxs-lookup"><span data-stu-id="69f44-105">DESCRIPTION</span></span>
<span data-ttu-id="69f44-106">**Wait-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업이 완료될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="69f44-107">예제</span><span class="sxs-lookup"><span data-stu-id="69f44-107">EXAMPLES</span></span>

### <span data-ttu-id="69f44-108">예제 1: 작업이 완료될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="69f44-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="69f44-109">다음 명령은 지정된 ID를 사용하여 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="69f44-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69f44-110">PARAMETERS</span></span>

### <span data-ttu-id="69f44-111">-Account</span><span class="sxs-lookup"><span data-stu-id="69f44-111">-Account</span></span>
<span data-ttu-id="69f44-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="69f44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f44-113">-DefaultProfile</span></span>
<span data-ttu-id="69f44-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="69f44-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69f44-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="69f44-115">-JobId</span></span>
<span data-ttu-id="69f44-116">대기할 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="69f44-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="69f44-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="69f44-118">대기 작업을 종료하기 전에 대기할 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="69f44-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="69f44-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="69f44-120">작업 상태의 각 검사 사이에 경과되는 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="69f44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f44-121">CommonParameters</span></span>
<span data-ttu-id="69f44-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69f44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f44-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="69f44-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f44-124">입력</span><span class="sxs-lookup"><span data-stu-id="69f44-124">INPUTS</span></span>

### <span data-ttu-id="69f44-125">System.String</span><span class="sxs-lookup"><span data-stu-id="69f44-125">System.String</span></span>

### <span data-ttu-id="69f44-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="69f44-126">System.Guid</span></span>

### <span data-ttu-id="69f44-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="69f44-127">System.Int32</span></span>

## <span data-ttu-id="69f44-128">출력</span><span class="sxs-lookup"><span data-stu-id="69f44-128">OUTPUTS</span></span>

### <span data-ttu-id="69f44-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="69f44-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="69f44-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69f44-130">NOTES</span></span>

## <span data-ttu-id="69f44-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69f44-131">RELATED LINKS</span></span>

[<span data-ttu-id="69f44-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="69f44-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="69f44-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="69f44-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="69f44-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="69f44-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


