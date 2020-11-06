---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537491"
---
# <span data-ttu-id="b915e-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b915e-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="b915e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b915e-102">SYNOPSIS</span></span>
<span data-ttu-id="b915e-103">일괄 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b915e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b915e-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b915e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b915e-105">DESCRIPTION</span></span>
<span data-ttu-id="b915e-106">**-AzureBatchJobSchedule** Cmdlet을 사용 하면 Azure Batch 작업 일정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="b915e-107">작업 일정을 사용 하도록 설정한 후에는 해당 일정에 따라 작업을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="b915e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b915e-108">EXAMPLES</span></span>

### <span data-ttu-id="b915e-109">예제 1: 작업 일정 설정</span><span class="sxs-lookup"><span data-stu-id="b915e-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="b915e-110">이 명령은 ID JobSchedule17가 있는 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="b915e-111">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b915e-112">변수</span><span class="sxs-lookup"><span data-stu-id="b915e-112">PARAMETERS</span></span>

### <span data-ttu-id="b915e-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b915e-113">-BatchContext</span></span>
<span data-ttu-id="b915e-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b915e-115">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b915e-116">-Id</span><span class="sxs-lookup"><span data-stu-id="b915e-116">-Id</span></span>
<span data-ttu-id="b915e-117">이 cmdlet이 사용할 수 있는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="b915e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b915e-118">-DefaultProfile</span></span>
<span data-ttu-id="b915e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b915e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b915e-120">CommonParameters</span></span>
<span data-ttu-id="b915e-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b915e-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b915e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b915e-123">입력</span><span class="sxs-lookup"><span data-stu-id="b915e-123">INPUTS</span></span>

### <span data-ttu-id="b915e-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b915e-124">BatchAccountContext</span></span>
<span data-ttu-id="b915e-125">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b915e-126">이름</span><span class="sxs-lookup"><span data-stu-id="b915e-126">String</span></span>
<span data-ttu-id="b915e-127">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b915e-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b915e-128">출력</span><span class="sxs-lookup"><span data-stu-id="b915e-128">OUTPUTS</span></span>

## <span data-ttu-id="b915e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b915e-129">NOTES</span></span>

## <span data-ttu-id="b915e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b915e-130">RELATED LINKS</span></span>

[<span data-ttu-id="b915e-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b915e-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b915e-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b915e-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b915e-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b915e-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="b915e-134">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b915e-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="b915e-135">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="b915e-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="b915e-136">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b915e-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="b915e-137">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b915e-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


