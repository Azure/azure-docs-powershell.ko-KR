---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711618"
---
# <span data-ttu-id="c7539-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c7539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7539-102">SYNOPSIS</span></span>
<span data-ttu-id="c7539-103">작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7539-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7539-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7539-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7539-105">DESCRIPTION</span></span>
<span data-ttu-id="c7539-106">**Set-AzureBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="c7539-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c7539-107">EXAMPLES</span></span>

## <span data-ttu-id="c7539-108">변수</span><span class="sxs-lookup"><span data-stu-id="c7539-108">PARAMETERS</span></span>

### <span data-ttu-id="c7539-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c7539-109">-BatchContext</span></span>
<span data-ttu-id="c7539-110">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c7539-111">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c7539-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-112">-JobSchedule</span></span>
<span data-ttu-id="c7539-113">작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="c7539-114">**Pscloudjobschedule** 개체를 얻으려면 Get-AzureBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="c7539-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7539-115">-DefaultProfile</span></span>
<span data-ttu-id="c7539-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7539-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7539-117">CommonParameters</span></span>
<span data-ttu-id="c7539-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7539-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7539-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7539-120">입력</span><span class="sxs-lookup"><span data-stu-id="c7539-120">INPUTS</span></span>

### <span data-ttu-id="c7539-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c7539-121">BatchAccountContext</span></span>
<span data-ttu-id="c7539-122">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c7539-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="c7539-124">' JobSchedule ' 매개 변수는 파이프라인에서 ' PSCloudJobSchedule ' 형식의 값을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="c7539-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="c7539-125">출력</span><span class="sxs-lookup"><span data-stu-id="c7539-125">OUTPUTS</span></span>

## <span data-ttu-id="c7539-126">상속자</span><span class="sxs-lookup"><span data-stu-id="c7539-126">NOTES</span></span>

## <span data-ttu-id="c7539-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7539-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7539-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c7539-129">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="c7539-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c7539-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="c7539-131">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c7539-132">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="c7539-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c7539-133">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7539-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


