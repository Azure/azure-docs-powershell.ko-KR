---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527060"
---
# <span data-ttu-id="ac73a-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ac73a-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="ac73a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac73a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac73a-103">풀 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac73a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac73a-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac73a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac73a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac73a-106">**Stop-AzureBatchPoolResize** cmdlet은 풀에서 Azure 일괄 처리 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="ac73a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac73a-107">EXAMPLES</span></span>

### <span data-ttu-id="ac73a-108">예제 1: 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="ac73a-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="ac73a-109">이 명령은 ID ContosoPool06가 있는 풀에서 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="ac73a-110">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ac73a-111">예제 2: 파이프라인을 사용 하 여 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="ac73a-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="ac73a-112">이 명령은 파이프라인 연산자를 사용 하 여 풀 크기 조정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="ac73a-113">명령은 Get-AzureBatchPool cmdlet을 사용 하 여 ID ContosoPool06 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="ac73a-114">명령이 현재 cmdlet에 해당 풀 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="ac73a-115">이 명령은 해당 풀의 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="ac73a-116">변수</span><span class="sxs-lookup"><span data-stu-id="ac73a-116">PARAMETERS</span></span>

### <span data-ttu-id="ac73a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ac73a-117">-BatchContext</span></span>
<span data-ttu-id="ac73a-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ac73a-119">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ac73a-120">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ac73a-121">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ac73a-122">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ac73a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac73a-123">-DefaultProfile</span></span>
<span data-ttu-id="ac73a-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac73a-125">-Id</span><span class="sxs-lookup"><span data-stu-id="ac73a-125">-Id</span></span>
<span data-ttu-id="ac73a-126">이 cmdlet이 크기 조정 작업을 중지 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="ac73a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac73a-127">CommonParameters</span></span>
<span data-ttu-id="ac73a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac73a-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac73a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac73a-130">입력</span><span class="sxs-lookup"><span data-stu-id="ac73a-130">INPUTS</span></span>

### <span data-ttu-id="ac73a-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ac73a-131">BatchAccountContext</span></span>
<span data-ttu-id="ac73a-132">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ac73a-133">이름</span><span class="sxs-lookup"><span data-stu-id="ac73a-133">String</span></span>
<span data-ttu-id="ac73a-134">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac73a-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ac73a-135">출력</span><span class="sxs-lookup"><span data-stu-id="ac73a-135">OUTPUTS</span></span>

## <span data-ttu-id="ac73a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ac73a-136">NOTES</span></span>

## <span data-ttu-id="ac73a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac73a-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac73a-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ac73a-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ac73a-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ac73a-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="ac73a-140">시작-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ac73a-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="ac73a-141">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac73a-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


