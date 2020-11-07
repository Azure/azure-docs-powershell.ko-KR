---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 302129506c516cd0f2864210d5323b83fb54e0df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702960"
---
# <span data-ttu-id="2b30d-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2b30d-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="2b30d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b30d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b30d-103">작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b30d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b30d-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b30d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b30d-105">DESCRIPTION</span></span>
<span data-ttu-id="2b30d-106">**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake Analytics 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="2b30d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b30d-107">EXAMPLES</span></span>

### <span data-ttu-id="2b30d-108">예제 1: 작업이 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="2b30d-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="2b30d-109">다음 명령은 지정 된 ID의 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="2b30d-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b30d-110">PARAMETERS</span></span>

### <span data-ttu-id="2b30d-111">-계정</span><span class="sxs-lookup"><span data-stu-id="2b30d-111">-Account</span></span>
<span data-ttu-id="2b30d-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2b30d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b30d-113">-DefaultProfile</span></span>
<span data-ttu-id="2b30d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b30d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b30d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="2b30d-115">-JobId</span></span>
<span data-ttu-id="2b30d-116">대기할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="2b30d-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2b30d-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="2b30d-118">대기 작업을 종료 하기 전에 대기할 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="2b30d-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2b30d-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="2b30d-120">각 작업 상태를 확인할 때 까지의 경과 시간을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="2b30d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b30d-121">CommonParameters</span></span>
<span data-ttu-id="2b30d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b30d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b30d-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b30d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b30d-124">입력</span><span class="sxs-lookup"><span data-stu-id="2b30d-124">INPUTS</span></span>

### <span data-ttu-id="2b30d-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b30d-125">System.String</span></span>

### <span data-ttu-id="2b30d-126">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="2b30d-126">System.Guid</span></span>

### <span data-ttu-id="2b30d-127">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="2b30d-127">System.Int32</span></span>

## <span data-ttu-id="2b30d-128">출력</span><span class="sxs-lookup"><span data-stu-id="2b30d-128">OUTPUTS</span></span>

### <span data-ttu-id="2b30d-129">DataLake에 대 한 정보를 보려면</span><span class="sxs-lookup"><span data-stu-id="2b30d-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="2b30d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2b30d-130">NOTES</span></span>

## <span data-ttu-id="2b30d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b30d-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b30d-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2b30d-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="2b30d-133">중지-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2b30d-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="2b30d-134">제출-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2b30d-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


