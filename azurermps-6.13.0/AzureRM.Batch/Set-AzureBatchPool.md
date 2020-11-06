---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524575"
---
# <span data-ttu-id="6c37c-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6c37c-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="6c37c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c37c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c37c-103">풀의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c37c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c37c-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c37c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6c37c-105">DESCRIPTION</span></span>
<span data-ttu-id="6c37c-106">**Set-AzureBatchPool** Cmdlet은 Azure Batch service에서 풀의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="6c37c-107">**Pscloudpool** 개체를 가져오려면 Get-AzureBatchPool cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="6c37c-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="6c37c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6c37c-109">EXAMPLES</span></span>

### <span data-ttu-id="6c37c-110">예제 1: 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="6c37c-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="6c37c-111">첫 번째 명령은 **Get-AzureBatchPool** 를 사용 하 여 풀을 가져온 다음 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="6c37c-112">다음 세 개의 명령은 $Pool 개체에 대 한 시작 작업 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="6c37c-113">마지막 명령은 $Pool의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="6c37c-114">변수</span><span class="sxs-lookup"><span data-stu-id="6c37c-114">PARAMETERS</span></span>

### <span data-ttu-id="6c37c-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6c37c-115">-BatchContext</span></span>
<span data-ttu-id="6c37c-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6c37c-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6c37c-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6c37c-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6c37c-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6c37c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c37c-121">-DefaultProfile</span></span>
<span data-ttu-id="6c37c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c37c-123">-풀</span><span class="sxs-lookup"><span data-stu-id="6c37c-123">-Pool</span></span>
<span data-ttu-id="6c37c-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudpool** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c37c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c37c-125">CommonParameters</span></span>
<span data-ttu-id="6c37c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c37c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c37c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c37c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c37c-128">입력</span><span class="sxs-lookup"><span data-stu-id="6c37c-128">INPUTS</span></span>

### <span data-ttu-id="6c37c-129">Microsoft.Azure.Commands.Batch. PSCloudPool 모델</span><span class="sxs-lookup"><span data-stu-id="6c37c-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="6c37c-130">매개 변수: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c37c-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="6c37c-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6c37c-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6c37c-132">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c37c-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6c37c-133">출력</span><span class="sxs-lookup"><span data-stu-id="6c37c-133">OUTPUTS</span></span>

### <span data-ttu-id="6c37c-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6c37c-134">System.Void</span></span>

## <span data-ttu-id="6c37c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6c37c-135">NOTES</span></span>

## <span data-ttu-id="6c37c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c37c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c37c-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6c37c-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="6c37c-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6c37c-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6c37c-139">새-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6c37c-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="6c37c-140">-AzureBatchPool 제거</span><span class="sxs-lookup"><span data-stu-id="6c37c-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="6c37c-141">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6c37c-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


