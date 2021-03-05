---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: 8b0bf38d68f4dbab815b6de1f056439cd5e88e3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008128"
---
# <span data-ttu-id="6ecec-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6ecec-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="6ecec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ecec-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecec-103">풀의 자동 크기 조정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="6ecec-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ecec-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ecec-105">설명</span><span class="sxs-lookup"><span data-stu-id="6ecec-105">DESCRIPTION</span></span>
<span data-ttu-id="6ecec-106">**Disable-AzBatchAutoScale** cmdlet은 지정된 풀의 자동 크기 조정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="6ecec-107">예제</span><span class="sxs-lookup"><span data-stu-id="6ecec-107">EXAMPLES</span></span>

### <span data-ttu-id="6ecec-108">예제 1: 풀의 자동 크기 조정 비활성화</span><span class="sxs-lookup"><span data-stu-id="6ecec-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="6ecec-109">이 명령은 MyPool이라는 풀에 대한 자동 크기 조정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="6ecec-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ecec-110">PARAMETERS</span></span>

### <span data-ttu-id="6ecec-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6ecec-111">-BatchContext</span></span>
<span data-ttu-id="6ecec-112">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ecec-113">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6ecec-114">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6ecec-115">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6ecec-116">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6ecec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecec-117">-DefaultProfile</span></span>
<span data-ttu-id="6ecec-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ecec-119">-Id</span><span class="sxs-lookup"><span data-stu-id="6ecec-119">-Id</span></span>
<span data-ttu-id="6ecec-120">풀의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="6ecec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecec-121">CommonParameters</span></span>
<span data-ttu-id="6ecec-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ecec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecec-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ecec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecec-124">입력</span><span class="sxs-lookup"><span data-stu-id="6ecec-124">INPUTS</span></span>

### <span data-ttu-id="6ecec-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6ecec-125">System.String</span></span>

### <span data-ttu-id="6ecec-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6ecec-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6ecec-127">출력</span><span class="sxs-lookup"><span data-stu-id="6ecec-127">OUTPUTS</span></span>

### <span data-ttu-id="6ecec-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="6ecec-128">System.Void</span></span>

## <span data-ttu-id="6ecec-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ecec-129">NOTES</span></span>

## <span data-ttu-id="6ecec-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ecec-130">RELATED LINKS</span></span>

[<span data-ttu-id="6ecec-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6ecec-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="6ecec-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="6ecec-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="6ecec-133">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ecec-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


