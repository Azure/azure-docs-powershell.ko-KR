---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 81ace9fd18b916f8f4788cf5878af1a620a61882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704038"
---
# <span data-ttu-id="2a575-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a575-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="2a575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a575-102">SYNOPSIS</span></span>
<span data-ttu-id="2a575-103">일괄 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a575-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a575-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a575-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a575-105">DESCRIPTION</span></span>
<span data-ttu-id="2a575-106">**Enable-AzureBatchJob** Cmdlet은 Azure 일괄 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="2a575-107">작업을 사용 하도록 설정한 후에는 새 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="2a575-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2a575-108">EXAMPLES</span></span>

### <span data-ttu-id="2a575-109">예제 1: 일괄 처리 작업 사용</span><span class="sxs-lookup"><span data-stu-id="2a575-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="2a575-110">이 명령을 사용 하면 ID 작업이 있는 작업을 000001 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2a575-111">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2a575-112">변수</span><span class="sxs-lookup"><span data-stu-id="2a575-112">PARAMETERS</span></span>

### <span data-ttu-id="2a575-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2a575-113">-BatchContext</span></span>
<span data-ttu-id="2a575-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2a575-115">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2a575-116">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2a575-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2a575-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2a575-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a575-119">-DefaultProfile</span></span>
<span data-ttu-id="2a575-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a575-121">-Id</span><span class="sxs-lookup"><span data-stu-id="2a575-121">-Id</span></span>
<span data-ttu-id="2a575-122">이 cmdlet이 사용할 수 있는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="2a575-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a575-123">CommonParameters</span></span>
<span data-ttu-id="2a575-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a575-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a575-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a575-126">입력</span><span class="sxs-lookup"><span data-stu-id="2a575-126">INPUTS</span></span>

### <span data-ttu-id="2a575-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2a575-127">BatchAccountContext</span></span>
<span data-ttu-id="2a575-128">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2a575-129">이름</span><span class="sxs-lookup"><span data-stu-id="2a575-129">String</span></span>
<span data-ttu-id="2a575-130">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a575-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2a575-131">출력</span><span class="sxs-lookup"><span data-stu-id="2a575-131">OUTPUTS</span></span>

## <span data-ttu-id="2a575-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2a575-132">NOTES</span></span>

## <span data-ttu-id="2a575-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a575-133">RELATED LINKS</span></span>

[<span data-ttu-id="2a575-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a575-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="2a575-135">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a575-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="2a575-136">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a575-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="2a575-137">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="2a575-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="2a575-138">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a575-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="2a575-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2a575-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


