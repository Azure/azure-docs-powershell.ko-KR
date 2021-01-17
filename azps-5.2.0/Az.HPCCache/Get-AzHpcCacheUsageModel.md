---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322804"
---
# <span data-ttu-id="14a4a-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="14a4a-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="14a4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="14a4a-103">NFS 저장소 대상에 대한 모든 usageModels를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14a4a-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="14a4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="14a4a-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14a4a-105">설명</span><span class="sxs-lookup"><span data-stu-id="14a4a-105">DESCRIPTION</span></span>
<span data-ttu-id="14a4a-106">**Get-AzHpcCacheUsageModel cmdlet은** NFS 저장소 대상에 대한 사용 모델 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="14a4a-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="14a4a-107">예제</span><span class="sxs-lookup"><span data-stu-id="14a4a-107">EXAMPLES</span></span>

### <span data-ttu-id="14a4a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14a4a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="14a4a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14a4a-109">PARAMETERS</span></span>

### <span data-ttu-id="14a4a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a4a-110">-DefaultProfile</span></span>
<span data-ttu-id="14a4a-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14a4a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a4a-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a4a-112">CommonParameters</span></span>
<span data-ttu-id="14a4a-113">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14a4a-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a4a-114">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14a4a-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a4a-115">입력</span><span class="sxs-lookup"><span data-stu-id="14a4a-115">INPUTS</span></span>

### <span data-ttu-id="14a4a-116">없음</span><span class="sxs-lookup"><span data-stu-id="14a4a-116">None</span></span>

## <span data-ttu-id="14a4a-117">출력</span><span class="sxs-lookup"><span data-stu-id="14a4a-117">OUTPUTS</span></span>

### <span data-ttu-id="14a4a-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="14a4a-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="14a4a-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="14a4a-119">System.Object</span></span>
## <span data-ttu-id="14a4a-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14a4a-120">NOTES</span></span>

## <span data-ttu-id="14a4a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14a4a-121">RELATED LINKS</span></span>
