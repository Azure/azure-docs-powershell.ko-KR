---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: d8ce1ec138decb5769aebba431db2accd671f100
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532332"
---
# <span data-ttu-id="5a799-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5a799-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="5a799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a799-102">SYNOPSIS</span></span>
<span data-ttu-id="5a799-103">풀 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a799-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a799-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a799-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a799-105">DESCRIPTION</span></span>
<span data-ttu-id="5a799-106">**Stop-AzureBatchPoolResize** cmdlet은 풀에서 Azure 일괄 처리 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="5a799-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5a799-107">EXAMPLES</span></span>

### <span data-ttu-id="5a799-108">예제 1: 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="5a799-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="5a799-109">이 명령은 ID ContosoPool06가 있는 풀에서 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="5a799-110">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5a799-111">예제 2: 파이프라인을 사용 하 여 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="5a799-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="5a799-112">이 명령은 파이프라인 연산자를 사용 하 여 풀 크기 조정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="5a799-113">명령은 Get-AzureBatchPool cmdlet을 사용 하 여 ID ContosoPool06 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="5a799-114">명령이 현재 cmdlet에 해당 풀 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="5a799-115">이 명령은 해당 풀의 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="5a799-116">변수</span><span class="sxs-lookup"><span data-stu-id="5a799-116">PARAMETERS</span></span>

### <span data-ttu-id="5a799-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5a799-117">-BatchContext</span></span>
<span data-ttu-id="5a799-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5a799-119">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5a799-120">-Id</span><span class="sxs-lookup"><span data-stu-id="5a799-120">-Id</span></span>
<span data-ttu-id="5a799-121">이 cmdlet이 크기 조정 작업을 중지 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-121">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="5a799-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a799-122">-DefaultProfile</span></span>
<span data-ttu-id="5a799-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a799-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a799-124">CommonParameters</span></span>
<span data-ttu-id="5a799-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a799-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a799-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a799-127">입력</span><span class="sxs-lookup"><span data-stu-id="5a799-127">INPUTS</span></span>

### <span data-ttu-id="5a799-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5a799-128">BatchAccountContext</span></span>
<span data-ttu-id="5a799-129">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5a799-130">이름</span><span class="sxs-lookup"><span data-stu-id="5a799-130">String</span></span>
<span data-ttu-id="5a799-131">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a799-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5a799-132">출력</span><span class="sxs-lookup"><span data-stu-id="5a799-132">OUTPUTS</span></span>

## <span data-ttu-id="5a799-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5a799-133">NOTES</span></span>

## <span data-ttu-id="5a799-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a799-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a799-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5a799-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5a799-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5a799-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="5a799-137">시작-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5a799-137">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="5a799-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a799-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


