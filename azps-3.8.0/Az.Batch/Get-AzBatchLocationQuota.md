---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044132"
---
# <span data-ttu-id="f26b2-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="f26b2-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="f26b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f26b2-103">지정 된 위치에서 구독에 대 한 일괄 처리 서비스 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="f26b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f26b2-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f26b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f26b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f26b2-106">주어진 위치에서 지정 된 구독에 대 한 일괄 처리 서비스 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="f26b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f26b2-107">EXAMPLES</span></span>

### <span data-ttu-id="f26b2-108">예제 1: 미국 지역에서 구독에 대 한 일괄 처리 서비스 할당량 가져오기</span><span class="sxs-lookup"><span data-stu-id="f26b2-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="f26b2-109">이 명령은 경기도 지역의 현재 구독에 대 한 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="f26b2-110">반환 값은이 구독이 해당 지역에 하나의 일괄 계정만 만들 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="f26b2-111">변수</span><span class="sxs-lookup"><span data-stu-id="f26b2-111">PARAMETERS</span></span>

### <span data-ttu-id="f26b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26b2-112">-DefaultProfile</span></span>
<span data-ttu-id="f26b2-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f26b2-114">-위치</span><span class="sxs-lookup"><span data-stu-id="f26b2-114">-Location</span></span>
<span data-ttu-id="f26b2-115">이 cmdlet이 할당량을 확인할 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="f26b2-116">자세한 내용은 Azure 지역 ()을 참조 하세요 https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="f26b2-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f26b2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26b2-117">CommonParameters</span></span>
<span data-ttu-id="f26b2-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f26b2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26b2-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f26b2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26b2-120">입력</span><span class="sxs-lookup"><span data-stu-id="f26b2-120">INPUTS</span></span>

### <span data-ttu-id="f26b2-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f26b2-121">System.String</span></span>

## <span data-ttu-id="f26b2-122">출력</span><span class="sxs-lookup"><span data-stu-id="f26b2-122">OUTPUTS</span></span>

### <span data-ttu-id="f26b2-123">Microsoft.Azure.Commands.Batch. PSBatchLocationQuotas 모델</span><span class="sxs-lookup"><span data-stu-id="f26b2-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="f26b2-124">상속자</span><span class="sxs-lookup"><span data-stu-id="f26b2-124">NOTES</span></span>

## <span data-ttu-id="f26b2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f26b2-125">RELATED LINKS</span></span>