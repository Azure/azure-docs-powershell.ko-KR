---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: e84bf86a3a784e47088ff1ed71047faac99239f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531461"
---
# <span data-ttu-id="892f6-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="892f6-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="892f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="892f6-102">SYNOPSIS</span></span>
<span data-ttu-id="892f6-103">일괄 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="892f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="892f6-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="892f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="892f6-105">DESCRIPTION</span></span>
<span data-ttu-id="892f6-106">**-AzureBatchJobSchedule** Cmdlet을 사용 하면 Azure Batch 작업 일정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="892f6-107">작업 일정을 사용 하도록 설정한 후에는 해당 일정에 따라 작업을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="892f6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="892f6-108">EXAMPLES</span></span>

### <span data-ttu-id="892f6-109">예제 1: 작업 일정 설정</span><span class="sxs-lookup"><span data-stu-id="892f6-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="892f6-110">이 명령은 ID JobSchedule17가 있는 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="892f6-111">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="892f6-112">변수</span><span class="sxs-lookup"><span data-stu-id="892f6-112">PARAMETERS</span></span>

### <span data-ttu-id="892f6-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="892f6-113">-BatchContext</span></span>
<span data-ttu-id="892f6-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="892f6-115">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="892f6-116">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="892f6-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="892f6-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="892f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892f6-119">-DefaultProfile</span></span>
<span data-ttu-id="892f6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="892f6-121">-Id</span><span class="sxs-lookup"><span data-stu-id="892f6-121">-Id</span></span>
<span data-ttu-id="892f6-122">이 cmdlet이 사용할 수 있는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="892f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892f6-123">CommonParameters</span></span>
<span data-ttu-id="892f6-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892f6-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892f6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892f6-126">입력</span><span class="sxs-lookup"><span data-stu-id="892f6-126">INPUTS</span></span>

### <span data-ttu-id="892f6-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="892f6-127">System.String</span></span>

### <span data-ttu-id="892f6-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="892f6-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="892f6-129">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="892f6-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="892f6-130">출력</span><span class="sxs-lookup"><span data-stu-id="892f6-130">OUTPUTS</span></span>

### <span data-ttu-id="892f6-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="892f6-131">System.Void</span></span>

## <span data-ttu-id="892f6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="892f6-132">NOTES</span></span>

## <span data-ttu-id="892f6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="892f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="892f6-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="892f6-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="892f6-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="892f6-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="892f6-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="892f6-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="892f6-137">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="892f6-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="892f6-138">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="892f6-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="892f6-139">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="892f6-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="892f6-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="892f6-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


