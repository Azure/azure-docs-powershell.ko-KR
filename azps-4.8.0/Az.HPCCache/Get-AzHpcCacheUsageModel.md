---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056332"
---
# <span data-ttu-id="057f7-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="057f7-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="057f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="057f7-102">SYNOPSIS</span></span>
<span data-ttu-id="057f7-103">NFS 용 모든 저장소 대상에 대 한 모든 usageModels를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="057f7-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="057f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="057f7-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="057f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="057f7-105">DESCRIPTION</span></span>
<span data-ttu-id="057f7-106">**AzHpcCacheUsageModel** CMDLET은 NFS 저장소 대상에 대 한 사용 모델 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="057f7-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="057f7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="057f7-107">EXAMPLES</span></span>

### <span data-ttu-id="057f7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="057f7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="057f7-109">변수</span><span class="sxs-lookup"><span data-stu-id="057f7-109">PARAMETERS</span></span>

### <span data-ttu-id="057f7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057f7-110">-DefaultProfile</span></span>
<span data-ttu-id="057f7-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="057f7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="057f7-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057f7-112">CommonParameters</span></span>
<span data-ttu-id="057f7-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="057f7-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057f7-114">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="057f7-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057f7-115">입력</span><span class="sxs-lookup"><span data-stu-id="057f7-115">INPUTS</span></span>

### <span data-ttu-id="057f7-116">않아야</span><span class="sxs-lookup"><span data-stu-id="057f7-116">None</span></span>

## <span data-ttu-id="057f7-117">출력</span><span class="sxs-lookup"><span data-stu-id="057f7-117">OUTPUTS</span></span>

### <span data-ttu-id="057f7-118">Microsoft. PowerShell. d s l e. e 2 pcpc</span><span class="sxs-lookup"><span data-stu-id="057f7-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="057f7-119">System. 개체</span><span class="sxs-lookup"><span data-stu-id="057f7-119">System.Object</span></span>
## <span data-ttu-id="057f7-120">상속자</span><span class="sxs-lookup"><span data-stu-id="057f7-120">NOTES</span></span>

## <span data-ttu-id="057f7-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="057f7-121">RELATED LINKS</span></span>
