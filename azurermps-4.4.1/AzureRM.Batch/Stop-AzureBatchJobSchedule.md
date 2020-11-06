---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532335"
---
# <span data-ttu-id="cbb41-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbb41-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="cbb41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb41-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb41-103">일괄 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbb41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbb41-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cbb41-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb41-106">**Stop-AzureBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="cbb41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cbb41-107">EXAMPLES</span></span>

### <span data-ttu-id="cbb41-108">예제 1: 작업 일정 중지</span><span class="sxs-lookup"><span data-stu-id="cbb41-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="cbb41-109">이 명령은 ID JobSchedule17가 있는 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cbb41-110">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cbb41-111">변수</span><span class="sxs-lookup"><span data-stu-id="cbb41-111">PARAMETERS</span></span>

### <span data-ttu-id="cbb41-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cbb41-112">-BatchContext</span></span>
<span data-ttu-id="cbb41-113">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cbb41-114">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbb41-115">-Id</span><span class="sxs-lookup"><span data-stu-id="cbb41-115">-Id</span></span>
<span data-ttu-id="cbb41-116">이 cmdlet이 중지 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbb41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb41-117">-DefaultProfile</span></span>
<span data-ttu-id="cbb41-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbb41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb41-119">CommonParameters</span></span>
<span data-ttu-id="cbb41-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb41-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbb41-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb41-122">입력</span><span class="sxs-lookup"><span data-stu-id="cbb41-122">INPUTS</span></span>

### <span data-ttu-id="cbb41-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cbb41-123">BatchAccountContext</span></span>
<span data-ttu-id="cbb41-124">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cbb41-125">이름</span><span class="sxs-lookup"><span data-stu-id="cbb41-125">String</span></span>
<span data-ttu-id="cbb41-126">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb41-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cbb41-127">출력</span><span class="sxs-lookup"><span data-stu-id="cbb41-127">OUTPUTS</span></span>

## <span data-ttu-id="cbb41-128">상속자</span><span class="sxs-lookup"><span data-stu-id="cbb41-128">NOTES</span></span>

## <span data-ttu-id="cbb41-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbb41-129">RELATED LINKS</span></span>

[<span data-ttu-id="cbb41-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbb41-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbb41-131">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="cbb41-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbb41-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cbb41-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cbb41-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbb41-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbb41-134">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cbb41-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbb41-135">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="cbb41-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="cbb41-136">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbb41-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


