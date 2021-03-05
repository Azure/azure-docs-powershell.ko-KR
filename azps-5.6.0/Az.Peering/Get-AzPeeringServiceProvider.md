---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989464"
---
# <span data-ttu-id="ec49c-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ec49c-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="ec49c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec49c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec49c-103">Microsoft와 파트너 관계가 있는 피어링 서비스 공급자 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ec49c-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="ec49c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec49c-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec49c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec49c-105">DESCRIPTION</span></span>
<span data-ttu-id="ec49c-106">피어링 서비스 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="ec49c-106">List peering service providers</span></span>

## <span data-ttu-id="ec49c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec49c-107">EXAMPLES</span></span>

### <span data-ttu-id="ec49c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec49c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="ec49c-109">사용 가능한 피어링 서비스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec49c-109">Gets available peering service providers</span></span>

## <span data-ttu-id="ec49c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec49c-110">PARAMETERS</span></span>

### <span data-ttu-id="ec49c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec49c-111">-DefaultProfile</span></span>
<span data-ttu-id="ec49c-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec49c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec49c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec49c-113">CommonParameters</span></span>
<span data-ttu-id="ec49c-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec49c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec49c-115">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec49c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec49c-116">입력</span><span class="sxs-lookup"><span data-stu-id="ec49c-116">INPUTS</span></span>

### <span data-ttu-id="ec49c-117">없음</span><span class="sxs-lookup"><span data-stu-id="ec49c-117">None</span></span>

## <span data-ttu-id="ec49c-118">출력</span><span class="sxs-lookup"><span data-stu-id="ec49c-118">OUTPUTS</span></span>

### <span data-ttu-id="ec49c-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ec49c-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="ec49c-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec49c-120">NOTES</span></span>

## <span data-ttu-id="ec49c-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec49c-121">RELATED LINKS</span></span>
