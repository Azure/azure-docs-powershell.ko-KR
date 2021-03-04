---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 297b862cb9491c0659d5fd2ec5ab0da4fc071e4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959008"
---
# <span data-ttu-id="a178c-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="a178c-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="a178c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a178c-102">SYNOPSIS</span></span>
<span data-ttu-id="a178c-103">할당된 위치에서 구독에 대한 Batch 서비스 할당량(Batch 서비스 할당량)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="a178c-104">구문</span><span class="sxs-lookup"><span data-stu-id="a178c-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a178c-105">설명</span><span class="sxs-lookup"><span data-stu-id="a178c-105">DESCRIPTION</span></span>
<span data-ttu-id="a178c-106">지정된 위치에서 지정된 구독에 대한 Batch 서비스 할당량(Batch 서비스 할당량)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="a178c-107">예제</span><span class="sxs-lookup"><span data-stu-id="a178c-107">EXAMPLES</span></span>

### <span data-ttu-id="a178c-108">예제 1: 미국 서부 지역의 구독에 대한 Batch 서비스 할당량 확인</span><span class="sxs-lookup"><span data-stu-id="a178c-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="a178c-109">이 명령은 미국 서부 지역의 현재 구독에 대한 할당량(할당량)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="a178c-110">반환 값은 이 구독이 해당 지역에 하나의 Batch 계정만 만들 수 있는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="a178c-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a178c-111">PARAMETERS</span></span>

### <span data-ttu-id="a178c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a178c-112">-DefaultProfile</span></span>
<span data-ttu-id="a178c-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a178c-114">-Location</span><span class="sxs-lookup"><span data-stu-id="a178c-114">-Location</span></span>
<span data-ttu-id="a178c-115">이 cmdlet에서 할당량 확인을 하는 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="a178c-116">자세한 내용은 Azure https://azure.microsoft.com/regions) Regions(를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a178c-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="a178c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a178c-117">CommonParameters</span></span>
<span data-ttu-id="a178c-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a178c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a178c-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a178c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a178c-120">입력</span><span class="sxs-lookup"><span data-stu-id="a178c-120">INPUTS</span></span>

### <span data-ttu-id="a178c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a178c-121">System.String</span></span>

## <span data-ttu-id="a178c-122">출력</span><span class="sxs-lookup"><span data-stu-id="a178c-122">OUTPUTS</span></span>

### <span data-ttu-id="a178c-123">Microsoft.Azure.Commands.Bat. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="a178c-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="a178c-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a178c-124">NOTES</span></span>

## <span data-ttu-id="a178c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a178c-125">RELATED LINKS</span></span>
