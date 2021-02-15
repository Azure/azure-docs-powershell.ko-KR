---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195217"
---
# <span data-ttu-id="cb260-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cb260-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="cb260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb260-102">SYNOPSIS</span></span>
<span data-ttu-id="cb260-103">풀의 수리 작업 수행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="cb260-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb260-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb260-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb260-105">DESCRIPTION</span></span>
<span data-ttu-id="cb260-106">**Stop-AzBatchPoolResize** cmdlet은 풀에서 Azure Batch 크기 변경 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="cb260-107">예제</span><span class="sxs-lookup"><span data-stu-id="cb260-107">EXAMPLES</span></span>

### <span data-ttu-id="cb260-108">예제 1: 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="cb260-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="cb260-109">이 명령은 ID ContosoPool06이 있는 풀에서의 배정량 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="cb260-110">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context.</span><span class="sxs-lookup"><span data-stu-id="cb260-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cb260-111">예제 2: 파이프라인을 사용하여 풀 크기 조정 중지</span><span class="sxs-lookup"><span data-stu-id="cb260-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="cb260-112">이 명령은 파이프라인 연산자를 사용하여 풀의 크기 조정을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="cb260-113">이 명령은 Get-AzBatchPool cmdlet을 사용하여 ContosoPool06 ID가 있는 풀을 Get-AzBatchPool 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="cb260-114">이 명령은 풀 개체를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="cb260-115">이 명령은 이 풀에 대한 [재조정] 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="cb260-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb260-116">PARAMETERS</span></span>

### <span data-ttu-id="cb260-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cb260-117">-BatchContext</span></span>
<span data-ttu-id="cb260-118">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cb260-119">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cb260-120">대신 공유 키 인증을 사용Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cb260-121">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cb260-122">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cb260-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb260-123">-DefaultProfile</span></span>
<span data-ttu-id="cb260-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb260-125">-Id</span><span class="sxs-lookup"><span data-stu-id="cb260-125">-Id</span></span>
<span data-ttu-id="cb260-126">이 cmdlet이 크기 조정 작업을 중지하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="cb260-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb260-127">CommonParameters</span></span>
<span data-ttu-id="cb260-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb260-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb260-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb260-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb260-130">입력</span><span class="sxs-lookup"><span data-stu-id="cb260-130">INPUTS</span></span>

### <span data-ttu-id="cb260-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cb260-131">System.String</span></span>

### <span data-ttu-id="cb260-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cb260-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cb260-133">출력</span><span class="sxs-lookup"><span data-stu-id="cb260-133">OUTPUTS</span></span>

### <span data-ttu-id="cb260-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="cb260-134">System.Void</span></span>

## <span data-ttu-id="cb260-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb260-135">NOTES</span></span>

## <span data-ttu-id="cb260-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb260-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb260-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cb260-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cb260-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cb260-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="cb260-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cb260-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="cb260-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb260-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
