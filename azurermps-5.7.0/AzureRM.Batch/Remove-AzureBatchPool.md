---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: a42e6876336e409cca8df9e0fc72e65e8b6e1b3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535315"
---
# <span data-ttu-id="1d2e4-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="1d2e4-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="1d2e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2e4-103">지정 된 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d2e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d2e4-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d2e4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d2e4-105">DESCRIPTION</span></span>
<span data-ttu-id="1d2e4-106">**제거-AzureBatchPool** cmdlet은 지정 된 Azure 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="1d2e4-107">*Force* 매개 변수를 사용 하지 않는 경우 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="1d2e4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1d2e4-108">EXAMPLES</span></span>

### <span data-ttu-id="1d2e4-109">예제 1: 풀 ID를 기준으로 일괄 처리 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="1d2e4-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="1d2e4-110">이 명령은 ID MyPool를 사용 하 여 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="1d2e4-111">삭제 작업을 수행 하기 전에 사용자에 게 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="1d2e4-112">예제 2: 모든 일괄 처리 풀을 강제 삭제</span><span class="sxs-lookup"><span data-stu-id="1d2e4-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="1d2e4-113">이 명령은 모든 일괄 처리 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="1d2e4-114">*Force* 매개 변수가 있으므로 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="1d2e4-115">변수</span><span class="sxs-lookup"><span data-stu-id="1d2e4-115">PARAMETERS</span></span>

### <span data-ttu-id="1d2e4-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1d2e4-116">-BatchContext</span></span>
<span data-ttu-id="1d2e4-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1d2e4-118">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1d2e4-119">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1d2e4-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1d2e4-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1d2e4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2e4-122">-DefaultProfile</span></span>
<span data-ttu-id="1d2e4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d2e4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1d2e4-124">-Force</span></span>
<span data-ttu-id="1d2e4-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2e4-126">-Id</span><span class="sxs-lookup"><span data-stu-id="1d2e4-126">-Id</span></span>
<span data-ttu-id="1d2e4-127">삭제할 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="1d2e4-128">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2e4-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1d2e4-129">-Confirm</span></span>
<span data-ttu-id="1d2e4-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d2e4-131">-WhatIf</span></span>
<span data-ttu-id="1d2e4-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d2e4-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2e4-134">CommonParameters</span></span>
<span data-ttu-id="1d2e4-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2e4-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d2e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2e4-137">입력</span><span class="sxs-lookup"><span data-stu-id="1d2e4-137">INPUTS</span></span>

### <span data-ttu-id="1d2e4-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1d2e4-138">BatchAccountContext</span></span>
<span data-ttu-id="1d2e4-139">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d2e4-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="1d2e4-140">출력</span><span class="sxs-lookup"><span data-stu-id="1d2e4-140">OUTPUTS</span></span>

## <span data-ttu-id="1d2e4-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1d2e4-141">NOTES</span></span>

## <span data-ttu-id="1d2e4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d2e4-142">RELATED LINKS</span></span>

[<span data-ttu-id="1d2e4-143">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1d2e4-143">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1d2e4-144">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="1d2e4-144">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="1d2e4-145">새-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="1d2e4-145">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="1d2e4-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d2e4-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


