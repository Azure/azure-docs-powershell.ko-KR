---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347522"
---
# <span data-ttu-id="58542-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58542-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="58542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58542-102">SYNOPSIS</span></span>
<span data-ttu-id="58542-103">풀의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="58542-104">구문</span><span class="sxs-lookup"><span data-stu-id="58542-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58542-105">설명</span><span class="sxs-lookup"><span data-stu-id="58542-105">DESCRIPTION</span></span>
<span data-ttu-id="58542-106">**Set-AzBatchPool** cmdlet은 Azure Batch 서비스에서 풀의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="58542-107">Get-AzBatchPool cmdlet을 사용하여 **PSCloudPool 개체를** 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="58542-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="58542-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용하여 Batch 서비스에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="58542-109">예제</span><span class="sxs-lookup"><span data-stu-id="58542-109">EXAMPLES</span></span>

### <span data-ttu-id="58542-110">예제 1: 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="58542-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="58542-111">첫 번째 명령은 **Get-AzBatchPool을** 사용하여 풀을 끈 다음, $Pool 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="58542-112">다음 세 명령은 $Pool 개체에서 시작 태스크 사양을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="58542-113">마지막 명령은 Batch 서비스의 로컬 개체와 일치하게 Batch 서비스를 $Pool.</span><span class="sxs-lookup"><span data-stu-id="58542-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="58542-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58542-114">PARAMETERS</span></span>

### <span data-ttu-id="58542-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58542-115">-BatchContext</span></span>
<span data-ttu-id="58542-116">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58542-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="58542-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="58542-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="58542-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="58542-119">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="58542-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="58542-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="58542-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58542-121">-DefaultProfile</span></span>
<span data-ttu-id="58542-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58542-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58542-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="58542-123">-Pool</span></span>
<span data-ttu-id="58542-124">이 cmdlet이 Batch 서비스를 업데이트하는 **PSCloudPool을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="58542-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58542-125">CommonParameters</span></span>
<span data-ttu-id="58542-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58542-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58542-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58542-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58542-128">입력</span><span class="sxs-lookup"><span data-stu-id="58542-128">INPUTS</span></span>

### <span data-ttu-id="58542-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="58542-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="58542-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58542-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="58542-131">출력</span><span class="sxs-lookup"><span data-stu-id="58542-131">OUTPUTS</span></span>

### <span data-ttu-id="58542-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="58542-132">System.Void</span></span>

## <span data-ttu-id="58542-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58542-133">NOTES</span></span>

## <span data-ttu-id="58542-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58542-134">RELATED LINKS</span></span>

[<span data-ttu-id="58542-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58542-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="58542-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="58542-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="58542-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58542-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="58542-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58542-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="58542-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58542-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
