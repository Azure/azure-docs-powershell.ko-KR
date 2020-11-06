---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532504"
---
# <span data-ttu-id="2fe79-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe79-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="2fe79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fe79-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe79-103">일괄 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fe79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fe79-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe79-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2fe79-105">DESCRIPTION</span></span>
<span data-ttu-id="2fe79-106">**Stop-AzureBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="2fe79-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2fe79-107">EXAMPLES</span></span>

### <span data-ttu-id="2fe79-108">예제 1: 작업 일정 중지</span><span class="sxs-lookup"><span data-stu-id="2fe79-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="2fe79-109">이 명령은 ID JobSchedule17가 있는 작업 일정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="2fe79-110">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2fe79-111">변수</span><span class="sxs-lookup"><span data-stu-id="2fe79-111">PARAMETERS</span></span>

### <span data-ttu-id="2fe79-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2fe79-112">-BatchContext</span></span>
<span data-ttu-id="2fe79-113">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2fe79-114">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2fe79-115">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2fe79-116">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2fe79-117">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2fe79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe79-118">-DefaultProfile</span></span>
<span data-ttu-id="2fe79-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fe79-120">-Id</span><span class="sxs-lookup"><span data-stu-id="2fe79-120">-Id</span></span>
<span data-ttu-id="2fe79-121">이 cmdlet이 중지 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2fe79-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe79-122">CommonParameters</span></span>
<span data-ttu-id="2fe79-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe79-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe79-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe79-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe79-125">입력</span><span class="sxs-lookup"><span data-stu-id="2fe79-125">INPUTS</span></span>

### <span data-ttu-id="2fe79-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2fe79-126">System.String</span></span>

### <span data-ttu-id="2fe79-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2fe79-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="2fe79-128">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2fe79-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="2fe79-129">출력</span><span class="sxs-lookup"><span data-stu-id="2fe79-129">OUTPUTS</span></span>

### <span data-ttu-id="2fe79-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2fe79-130">System.Void</span></span>

## <span data-ttu-id="2fe79-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2fe79-131">NOTES</span></span>

## <span data-ttu-id="2fe79-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fe79-132">RELATED LINKS</span></span>

[<span data-ttu-id="2fe79-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe79-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="2fe79-134">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="2fe79-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="2fe79-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2fe79-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2fe79-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe79-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="2fe79-137">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe79-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="2fe79-138">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="2fe79-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="2fe79-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2fe79-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


