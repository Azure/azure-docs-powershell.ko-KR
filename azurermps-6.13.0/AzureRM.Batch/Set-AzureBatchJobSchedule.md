---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524579"
---
# <span data-ttu-id="b70bd-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b70bd-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="b70bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b70bd-103">작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b70bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b70bd-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b70bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b70bd-106">**Set-AzureBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="b70bd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b70bd-107">EXAMPLES</span></span>

## <span data-ttu-id="b70bd-108">변수</span><span class="sxs-lookup"><span data-stu-id="b70bd-108">PARAMETERS</span></span>

### <span data-ttu-id="b70bd-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b70bd-109">-BatchContext</span></span>
<span data-ttu-id="b70bd-110">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b70bd-111">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b70bd-112">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b70bd-113">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b70bd-114">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b70bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70bd-115">-DefaultProfile</span></span>
<span data-ttu-id="b70bd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b70bd-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="b70bd-117">-JobSchedule</span></span>
<span data-ttu-id="b70bd-118">작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="b70bd-119">**Pscloudjobschedule** 개체를 얻으려면 Get-AzureBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b70bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70bd-120">CommonParameters</span></span>
<span data-ttu-id="b70bd-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b70bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70bd-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70bd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70bd-123">입력</span><span class="sxs-lookup"><span data-stu-id="b70bd-123">INPUTS</span></span>

### <span data-ttu-id="b70bd-124">Microsoft.Azure.Commands.Batch. PSCloudJobSchedule 모델</span><span class="sxs-lookup"><span data-stu-id="b70bd-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="b70bd-125">매개 변수: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b70bd-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="b70bd-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b70bd-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b70bd-127">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b70bd-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b70bd-128">출력</span><span class="sxs-lookup"><span data-stu-id="b70bd-128">OUTPUTS</span></span>

### <span data-ttu-id="b70bd-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b70bd-129">System.Void</span></span>

## <span data-ttu-id="b70bd-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b70bd-130">NOTES</span></span>

## <span data-ttu-id="b70bd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b70bd-131">RELATED LINKS</span></span>

[<span data-ttu-id="b70bd-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b70bd-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b70bd-133">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="b70bd-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b70bd-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b70bd-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="b70bd-135">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b70bd-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="b70bd-136">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="b70bd-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="b70bd-137">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b70bd-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


