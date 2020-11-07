---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 9e970251671297a6fa4a0019bb663c9e34cbe4d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880054"
---
# <span data-ttu-id="c64aa-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c64aa-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="c64aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c64aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c64aa-103">풀 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="c64aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c64aa-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c64aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c64aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c64aa-106">**AzBatchPoolResize** cmdlet은 풀에서 Azure 일괄 처리 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="c64aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c64aa-107">EXAMPLES</span></span>

### <span data-ttu-id="c64aa-108">예제 1: 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="c64aa-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="c64aa-109">이 명령은 ID ContosoPool06가 있는 풀에서 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="c64aa-110">Get-AzBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c64aa-111">예제 2: 파이프라인을 사용 하 여 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="c64aa-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="c64aa-112">이 명령은 파이프라인 연산자를 사용 하 여 풀 크기 조정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="c64aa-113">명령은 Get-AzBatchPool cmdlet을 사용 하 여 ID ContosoPool06 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="c64aa-114">명령이 현재 cmdlet에 해당 풀 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="c64aa-115">이 명령은 해당 풀의 크기 조정 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="c64aa-116">변수</span><span class="sxs-lookup"><span data-stu-id="c64aa-116">PARAMETERS</span></span>

### <span data-ttu-id="c64aa-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c64aa-117">-BatchContext</span></span>
<span data-ttu-id="c64aa-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c64aa-119">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c64aa-120">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c64aa-121">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c64aa-122">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c64aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64aa-123">-DefaultProfile</span></span>
<span data-ttu-id="c64aa-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c64aa-125">-Id</span><span class="sxs-lookup"><span data-stu-id="c64aa-125">-Id</span></span>
<span data-ttu-id="c64aa-126">이 cmdlet이 크기 조정 작업을 중지 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="c64aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64aa-127">CommonParameters</span></span>
<span data-ttu-id="c64aa-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c64aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64aa-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64aa-130">입력</span><span class="sxs-lookup"><span data-stu-id="c64aa-130">INPUTS</span></span>

### <span data-ttu-id="c64aa-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c64aa-131">System.String</span></span>

### <span data-ttu-id="c64aa-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c64aa-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c64aa-133">출력</span><span class="sxs-lookup"><span data-stu-id="c64aa-133">OUTPUTS</span></span>

### <span data-ttu-id="c64aa-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c64aa-134">System.Void</span></span>

## <span data-ttu-id="c64aa-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c64aa-135">NOTES</span></span>

## <span data-ttu-id="c64aa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c64aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="c64aa-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c64aa-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c64aa-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="c64aa-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="c64aa-139">시작-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c64aa-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="c64aa-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c64aa-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


