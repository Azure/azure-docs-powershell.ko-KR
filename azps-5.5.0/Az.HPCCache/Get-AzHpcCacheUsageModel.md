---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209416"
---
# <span data-ttu-id="5338b-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="5338b-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="5338b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5338b-102">SYNOPSIS</span></span>
<span data-ttu-id="5338b-103">NFS 저장소 대상에 대한 모든 usageModels를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5338b-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="5338b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5338b-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5338b-105">설명</span><span class="sxs-lookup"><span data-stu-id="5338b-105">DESCRIPTION</span></span>
<span data-ttu-id="5338b-106">**Get-AzHpcCacheUsageModel** cmdlet은 NFS 저장소 대상에 대한 사용 모델 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5338b-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="5338b-107">예제</span><span class="sxs-lookup"><span data-stu-id="5338b-107">EXAMPLES</span></span>

### <span data-ttu-id="5338b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5338b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="5338b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5338b-109">PARAMETERS</span></span>

### <span data-ttu-id="5338b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5338b-110">-DefaultProfile</span></span>
<span data-ttu-id="5338b-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5338b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5338b-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5338b-112">CommonParameters</span></span>
<span data-ttu-id="5338b-113">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5338b-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5338b-114">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5338b-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5338b-115">입력</span><span class="sxs-lookup"><span data-stu-id="5338b-115">INPUTS</span></span>

### <span data-ttu-id="5338b-116">없음</span><span class="sxs-lookup"><span data-stu-id="5338b-116">None</span></span>

## <span data-ttu-id="5338b-117">출력</span><span class="sxs-lookup"><span data-stu-id="5338b-117">OUTPUTS</span></span>

### <span data-ttu-id="5338b-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="5338b-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="5338b-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="5338b-119">System.Object</span></span>
## <span data-ttu-id="5338b-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5338b-120">NOTES</span></span>

## <span data-ttu-id="5338b-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5338b-121">RELATED LINKS</span></span>
