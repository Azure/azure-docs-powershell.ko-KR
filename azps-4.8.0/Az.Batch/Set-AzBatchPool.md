---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049175"
---
# <span data-ttu-id="7a1c7-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a1c7-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="7a1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1c7-103">풀의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="7a1c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a1c7-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a1c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a1c7-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1c7-106">**AzBatchPool** Cmdlet은 Azure Batch 서비스에서 풀의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="7a1c7-107">**Pscloudpool** 개체를 가져오려면 Get-AzBatchPool cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="7a1c7-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="7a1c7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7a1c7-109">EXAMPLES</span></span>

### <span data-ttu-id="7a1c7-110">예제 1: 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="7a1c7-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="7a1c7-111">첫 번째 명령은 **Get-AzBatchPool** 를 사용 하 여 풀을 가져온 다음 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="7a1c7-112">다음 세 개의 명령은 $Pool 개체에 대 한 시작 작업 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="7a1c7-113">마지막 명령은 $Pool의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="7a1c7-114">변수</span><span class="sxs-lookup"><span data-stu-id="7a1c7-114">PARAMETERS</span></span>

### <span data-ttu-id="7a1c7-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7a1c7-115">-BatchContext</span></span>
<span data-ttu-id="7a1c7-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7a1c7-117">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7a1c7-118">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7a1c7-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7a1c7-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7a1c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1c7-121">-DefaultProfile</span></span>
<span data-ttu-id="7a1c7-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a1c7-123">-풀</span><span class="sxs-lookup"><span data-stu-id="7a1c7-123">-Pool</span></span>
<span data-ttu-id="7a1c7-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudpool** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="7a1c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1c7-125">CommonParameters</span></span>
<span data-ttu-id="7a1c7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1c7-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a1c7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1c7-128">입력</span><span class="sxs-lookup"><span data-stu-id="7a1c7-128">INPUTS</span></span>

### <span data-ttu-id="7a1c7-129">Microsoft.Azure.Commands.Batch. PSCloudPool 모델</span><span class="sxs-lookup"><span data-stu-id="7a1c7-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="7a1c7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7a1c7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7a1c7-131">출력</span><span class="sxs-lookup"><span data-stu-id="7a1c7-131">OUTPUTS</span></span>

### <span data-ttu-id="7a1c7-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="7a1c7-132">System.Void</span></span>

## <span data-ttu-id="7a1c7-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7a1c7-133">NOTES</span></span>

## <span data-ttu-id="7a1c7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a1c7-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a1c7-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a1c7-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="7a1c7-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7a1c7-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7a1c7-137">새로운 AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a1c7-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="7a1c7-138">제거-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a1c7-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="7a1c7-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a1c7-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
