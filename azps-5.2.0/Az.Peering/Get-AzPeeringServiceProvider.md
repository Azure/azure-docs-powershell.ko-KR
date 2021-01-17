---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336105"
---
# <span data-ttu-id="b70ca-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b70ca-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="b70ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b70ca-103">Microsoft와 파트너 관계에 있는 피어링 서비스 공급자 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b70ca-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="b70ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="b70ca-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70ca-105">설명</span><span class="sxs-lookup"><span data-stu-id="b70ca-105">DESCRIPTION</span></span>
<span data-ttu-id="b70ca-106">피어링 서비스 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="b70ca-106">List peering service providers</span></span>

## <span data-ttu-id="b70ca-107">예제</span><span class="sxs-lookup"><span data-stu-id="b70ca-107">EXAMPLES</span></span>

### <span data-ttu-id="b70ca-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b70ca-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="b70ca-109">사용 가능한 피어링 서비스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b70ca-109">Gets available peering service providers</span></span>

## <span data-ttu-id="b70ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b70ca-110">PARAMETERS</span></span>

### <span data-ttu-id="b70ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70ca-111">-DefaultProfile</span></span>
<span data-ttu-id="b70ca-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b70ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b70ca-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70ca-113">CommonParameters</span></span>
<span data-ttu-id="b70ca-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b70ca-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70ca-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b70ca-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70ca-116">입력</span><span class="sxs-lookup"><span data-stu-id="b70ca-116">INPUTS</span></span>

### <span data-ttu-id="b70ca-117">없음</span><span class="sxs-lookup"><span data-stu-id="b70ca-117">None</span></span>

## <span data-ttu-id="b70ca-118">출력</span><span class="sxs-lookup"><span data-stu-id="b70ca-118">OUTPUTS</span></span>

### <span data-ttu-id="b70ca-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b70ca-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="b70ca-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b70ca-120">NOTES</span></span>

## <span data-ttu-id="b70ca-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b70ca-121">RELATED LINKS</span></span>
