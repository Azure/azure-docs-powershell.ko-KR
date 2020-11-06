---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 85e47b9f9bea7a19bb11817c414e5d3b9a35d6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533708"
---
# <span data-ttu-id="e7dc2-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="e7dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="e7dc2-103">작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7dc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7dc2-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7dc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="e7dc2-106">**Set-AzureBatchJobSchedule** Cmdlet은 Azure Batch 서비스에서 작업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="e7dc2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7dc2-107">EXAMPLES</span></span>

## <span data-ttu-id="e7dc2-108">변수</span><span class="sxs-lookup"><span data-stu-id="e7dc2-108">PARAMETERS</span></span>

### <span data-ttu-id="e7dc2-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7dc2-109">-BatchContext</span></span>
<span data-ttu-id="e7dc2-110">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7dc2-111">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7dc2-112">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7dc2-113">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7dc2-114">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7dc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7dc2-115">-DefaultProfile</span></span>
<span data-ttu-id="e7dc2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7dc2-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-117">-JobSchedule</span></span>
<span data-ttu-id="e7dc2-118">작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="e7dc2-119">**Pscloudjobschedule** 개체를 얻으려면 Get-AzureBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7dc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7dc2-120">CommonParameters</span></span>
<span data-ttu-id="e7dc2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7dc2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7dc2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7dc2-123">입력</span><span class="sxs-lookup"><span data-stu-id="e7dc2-123">INPUTS</span></span>

### <span data-ttu-id="e7dc2-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7dc2-124">BatchAccountContext</span></span>
<span data-ttu-id="e7dc2-125">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e7dc2-126">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-126">PSCloudJobSchedule</span></span>
<span data-ttu-id="e7dc2-127">' JobSchedule ' 매개 변수는 파이프라인에서 ' PSCloudJobSchedule ' 형식의 값을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e7dc2-127">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="e7dc2-128">출력</span><span class="sxs-lookup"><span data-stu-id="e7dc2-128">OUTPUTS</span></span>

## <span data-ttu-id="e7dc2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e7dc2-129">NOTES</span></span>

## <span data-ttu-id="e7dc2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7dc2-130">RELATED LINKS</span></span>

[<span data-ttu-id="e7dc2-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e7dc2-132">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="e7dc2-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e7dc2-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="e7dc2-134">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="e7dc2-135">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="e7dc2-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="e7dc2-136">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7dc2-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


