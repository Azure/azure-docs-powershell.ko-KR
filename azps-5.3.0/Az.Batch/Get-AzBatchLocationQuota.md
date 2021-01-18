---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494149"
---
# <span data-ttu-id="98d8a-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="98d8a-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="98d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="98d8a-103">주어진 위치에서 구독에 대한 Batch 서비스 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="98d8a-104">구문</span><span class="sxs-lookup"><span data-stu-id="98d8a-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d8a-105">설명</span><span class="sxs-lookup"><span data-stu-id="98d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="98d8a-106">지정된 위치에서 지정된 구독에 대한 Batch 서비스 할당량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="98d8a-107">예제</span><span class="sxs-lookup"><span data-stu-id="98d8a-107">EXAMPLES</span></span>

### <span data-ttu-id="98d8a-108">예제 1: 미국 서부 지역의 구독에 대한 Batch 서비스 할당량 확인</span><span class="sxs-lookup"><span data-stu-id="98d8a-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="98d8a-109">이 명령은 미국 서부 지역의 현재 구독에 대한 할당량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="98d8a-110">반환 값은 이 구독이 해당 지역에 하나의 Batch 계정만 만들 수 있는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="98d8a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98d8a-111">PARAMETERS</span></span>

### <span data-ttu-id="98d8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d8a-112">-DefaultProfile</span></span>
<span data-ttu-id="98d8a-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d8a-114">-Location</span><span class="sxs-lookup"><span data-stu-id="98d8a-114">-Location</span></span>
<span data-ttu-id="98d8a-115">이 cmdlet이 할당량 확인을 하는 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="98d8a-116">자세한 내용은 Azure https://azure.microsoft.com/regions) 지역(.</span><span class="sxs-lookup"><span data-stu-id="98d8a-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="98d8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d8a-117">CommonParameters</span></span>
<span data-ttu-id="98d8a-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98d8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d8a-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98d8a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d8a-120">입력</span><span class="sxs-lookup"><span data-stu-id="98d8a-120">INPUTS</span></span>

### <span data-ttu-id="98d8a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="98d8a-121">System.String</span></span>

## <span data-ttu-id="98d8a-122">출력</span><span class="sxs-lookup"><span data-stu-id="98d8a-122">OUTPUTS</span></span>

### <span data-ttu-id="98d8a-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="98d8a-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="98d8a-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98d8a-124">NOTES</span></span>

## <span data-ttu-id="98d8a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98d8a-125">RELATED LINKS</span></span>
