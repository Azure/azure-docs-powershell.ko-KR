---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 51b7297aea0378b910d647f892a252a9b2ce494b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013547"
---
# <span data-ttu-id="4886e-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="4886e-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="4886e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4886e-102">SYNOPSIS</span></span>
<span data-ttu-id="4886e-103">NFS Storage 대상에 대한 모든 사용량모델을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4886e-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="4886e-104">구문</span><span class="sxs-lookup"><span data-stu-id="4886e-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4886e-105">설명</span><span class="sxs-lookup"><span data-stu-id="4886e-105">DESCRIPTION</span></span>
<span data-ttu-id="4886e-106">**Get-AzHpcCacheUsageModel cmdlet은** NFS Storage 대상에 대한 사용 모델 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4886e-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="4886e-107">예제</span><span class="sxs-lookup"><span data-stu-id="4886e-107">EXAMPLES</span></span>

### <span data-ttu-id="4886e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4886e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="4886e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4886e-109">PARAMETERS</span></span>

### <span data-ttu-id="4886e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4886e-110">-DefaultProfile</span></span>
<span data-ttu-id="4886e-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4886e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4886e-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4886e-112">CommonParameters</span></span>
<span data-ttu-id="4886e-113">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4886e-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4886e-114">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4886e-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4886e-115">입력</span><span class="sxs-lookup"><span data-stu-id="4886e-115">INPUTS</span></span>

### <span data-ttu-id="4886e-116">없음</span><span class="sxs-lookup"><span data-stu-id="4886e-116">None</span></span>

## <span data-ttu-id="4886e-117">출력</span><span class="sxs-lookup"><span data-stu-id="4886e-117">OUTPUTS</span></span>

### <span data-ttu-id="4886e-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="4886e-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="4886e-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="4886e-119">System.Object</span></span>
## <span data-ttu-id="4886e-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4886e-120">NOTES</span></span>

## <span data-ttu-id="4886e-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4886e-121">RELATED LINKS</span></span>
