---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: d20a52c3e907bd981bc0a692ebb4aa44495d0960
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880122"
---
# <span data-ttu-id="b86a6-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b86a6-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="b86a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b86a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b86a6-103">풀의 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="b86a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b86a6-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b86a6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b86a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b86a6-106">**AzBatchAutoScale** cmdlet은 지정 된 풀의 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="b86a6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b86a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b86a6-108">예제 1: 풀의 자동 크기 조정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b86a6-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="b86a6-109">이 명령은 MyPool 이라는 풀에 대해 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="b86a6-110">변수</span><span class="sxs-lookup"><span data-stu-id="b86a6-110">PARAMETERS</span></span>

### <span data-ttu-id="b86a6-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b86a6-111">-BatchContext</span></span>
<span data-ttu-id="b86a6-112">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b86a6-113">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b86a6-114">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b86a6-115">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b86a6-116">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b86a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86a6-117">-DefaultProfile</span></span>
<span data-ttu-id="b86a6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b86a6-119">-Id</span><span class="sxs-lookup"><span data-stu-id="b86a6-119">-Id</span></span>
<span data-ttu-id="b86a6-120">풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="b86a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86a6-121">CommonParameters</span></span>
<span data-ttu-id="b86a6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86a6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86a6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86a6-124">입력</span><span class="sxs-lookup"><span data-stu-id="b86a6-124">INPUTS</span></span>

### <span data-ttu-id="b86a6-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b86a6-125">System.String</span></span>

### <span data-ttu-id="b86a6-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b86a6-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b86a6-127">출력</span><span class="sxs-lookup"><span data-stu-id="b86a6-127">OUTPUTS</span></span>

### <span data-ttu-id="b86a6-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b86a6-128">System.Void</span></span>

## <span data-ttu-id="b86a6-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b86a6-129">NOTES</span></span>

## <span data-ttu-id="b86a6-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b86a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="b86a6-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b86a6-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="b86a6-132">테스트-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b86a6-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="b86a6-133">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b86a6-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


