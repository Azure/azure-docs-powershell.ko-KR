---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529852"
---
# <span data-ttu-id="e76ee-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e76ee-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="e76ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e76ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e76ee-103">작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e76ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e76ee-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e76ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e76ee-105">DESCRIPTION</span></span>
<span data-ttu-id="e76ee-106">**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="e76ee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e76ee-107">EXAMPLES</span></span>

### <span data-ttu-id="e76ee-108">예제 1: 작업 취소</span><span class="sxs-lookup"><span data-stu-id="e76ee-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="e76ee-109">이 명령은 지정 된 ID의 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="e76ee-110">변수</span><span class="sxs-lookup"><span data-stu-id="e76ee-110">PARAMETERS</span></span>

### <span data-ttu-id="e76ee-111">-계정</span><span class="sxs-lookup"><span data-stu-id="e76ee-111">-Account</span></span>
<span data-ttu-id="e76ee-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76ee-113">-DefaultProfile</span></span>
<span data-ttu-id="e76ee-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e76ee-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e76ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e76ee-115">-Force</span></span>
<span data-ttu-id="e76ee-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76ee-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="e76ee-117">-JobId</span></span>
<span data-ttu-id="e76ee-118">취소할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e76ee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e76ee-119">-PassThru</span></span>
<span data-ttu-id="e76ee-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e76ee-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76ee-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e76ee-122">-Confirm</span></span>
<span data-ttu-id="e76ee-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76ee-124">-WhatIf</span></span>
<span data-ttu-id="e76ee-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76ee-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76ee-127">CommonParameters</span></span>
<span data-ttu-id="e76ee-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76ee-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e76ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76ee-130">입력</span><span class="sxs-lookup"><span data-stu-id="e76ee-130">INPUTS</span></span>

### <span data-ttu-id="e76ee-131">Shap</span><span class="sxs-lookup"><span data-stu-id="e76ee-131">Guid</span></span>
<span data-ttu-id="e76ee-132">' JobId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="e76ee-133">출력</span><span class="sxs-lookup"><span data-stu-id="e76ee-133">OUTPUTS</span></span>

### <span data-ttu-id="e76ee-134">부울</span><span class="sxs-lookup"><span data-stu-id="e76ee-134">bool</span></span>
<span data-ttu-id="e76ee-135">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76ee-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="e76ee-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e76ee-136">NOTES</span></span>

## <span data-ttu-id="e76ee-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e76ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="e76ee-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e76ee-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="e76ee-139">제출-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e76ee-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="e76ee-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e76ee-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


