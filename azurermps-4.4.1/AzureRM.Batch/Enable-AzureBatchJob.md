---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711623"
---
# <span data-ttu-id="61f10-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="61f10-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="61f10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f10-102">SYNOPSIS</span></span>
<span data-ttu-id="61f10-103">일괄 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61f10-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61f10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="61f10-105">DESCRIPTION</span></span>
<span data-ttu-id="61f10-106">**Enable-AzureBatchJob** Cmdlet은 Azure 일괄 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="61f10-107">작업을 사용 하도록 설정한 후에는 새 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="61f10-108">예제의</span><span class="sxs-lookup"><span data-stu-id="61f10-108">EXAMPLES</span></span>

### <span data-ttu-id="61f10-109">예제 1: 일괄 처리 작업 사용</span><span class="sxs-lookup"><span data-stu-id="61f10-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="61f10-110">이 명령을 사용 하면 ID 작업이 있는 작업을 000001 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="61f10-111">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="61f10-112">변수</span><span class="sxs-lookup"><span data-stu-id="61f10-112">PARAMETERS</span></span>

### <span data-ttu-id="61f10-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="61f10-113">-BatchContext</span></span>
<span data-ttu-id="61f10-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="61f10-115">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="61f10-116">-Id</span><span class="sxs-lookup"><span data-stu-id="61f10-116">-Id</span></span>
<span data-ttu-id="61f10-117">이 cmdlet이 사용할 수 있는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="61f10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f10-118">-DefaultProfile</span></span>
<span data-ttu-id="61f10-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f10-120">CommonParameters</span></span>
<span data-ttu-id="61f10-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f10-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f10-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f10-123">입력</span><span class="sxs-lookup"><span data-stu-id="61f10-123">INPUTS</span></span>

### <span data-ttu-id="61f10-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="61f10-124">BatchAccountContext</span></span>
<span data-ttu-id="61f10-125">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="61f10-126">이름</span><span class="sxs-lookup"><span data-stu-id="61f10-126">String</span></span>
<span data-ttu-id="61f10-127">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f10-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="61f10-128">출력</span><span class="sxs-lookup"><span data-stu-id="61f10-128">OUTPUTS</span></span>

## <span data-ttu-id="61f10-129">상속자</span><span class="sxs-lookup"><span data-stu-id="61f10-129">NOTES</span></span>

## <span data-ttu-id="61f10-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61f10-130">RELATED LINKS</span></span>

[<span data-ttu-id="61f10-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="61f10-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="61f10-132">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="61f10-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="61f10-133">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="61f10-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="61f10-134">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="61f10-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="61f10-135">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="61f10-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="61f10-136">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="61f10-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


