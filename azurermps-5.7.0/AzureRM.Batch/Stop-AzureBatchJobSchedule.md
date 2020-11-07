---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 719c743281102f83c08f55093d221856be4194bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702174"
---
# <span data-ttu-id="aff77-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aff77-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="aff77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff77-102">SYNOPSIS</span></span>
<span data-ttu-id="aff77-103">일괄 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aff77-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aff77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aff77-105">DESCRIPTION</span></span>
<span data-ttu-id="aff77-106">**Stop-AzureBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="aff77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aff77-107">EXAMPLES</span></span>

### <span data-ttu-id="aff77-108">예제 1: 작업 일정 중지</span><span class="sxs-lookup"><span data-stu-id="aff77-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="aff77-109">이 명령은 ID JobSchedule17가 있는 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="aff77-110">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="aff77-111">변수</span><span class="sxs-lookup"><span data-stu-id="aff77-111">PARAMETERS</span></span>

### <span data-ttu-id="aff77-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aff77-112">-BatchContext</span></span>
<span data-ttu-id="aff77-113">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aff77-114">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aff77-115">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aff77-116">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aff77-117">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff77-118">-DefaultProfile</span></span>
<span data-ttu-id="aff77-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aff77-120">-Id</span><span class="sxs-lookup"><span data-stu-id="aff77-120">-Id</span></span>
<span data-ttu-id="aff77-121">이 cmdlet이 중지 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff77-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff77-122">CommonParameters</span></span>
<span data-ttu-id="aff77-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff77-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff77-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff77-125">입력</span><span class="sxs-lookup"><span data-stu-id="aff77-125">INPUTS</span></span>

### <span data-ttu-id="aff77-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aff77-126">BatchAccountContext</span></span>
<span data-ttu-id="aff77-127">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aff77-128">이름</span><span class="sxs-lookup"><span data-stu-id="aff77-128">String</span></span>
<span data-ttu-id="aff77-129">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff77-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="aff77-130">출력</span><span class="sxs-lookup"><span data-stu-id="aff77-130">OUTPUTS</span></span>

## <span data-ttu-id="aff77-131">상속자</span><span class="sxs-lookup"><span data-stu-id="aff77-131">NOTES</span></span>

## <span data-ttu-id="aff77-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aff77-132">RELATED LINKS</span></span>

[<span data-ttu-id="aff77-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aff77-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="aff77-134">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="aff77-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="aff77-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aff77-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aff77-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aff77-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="aff77-137">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aff77-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="aff77-138">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="aff77-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="aff77-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aff77-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


