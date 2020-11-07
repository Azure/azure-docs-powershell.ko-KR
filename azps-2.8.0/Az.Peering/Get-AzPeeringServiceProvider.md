---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 786a8009d1423b6b12fae4d7eb8da6899a8cd108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872385"
---
# <span data-ttu-id="655a1-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="655a1-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="655a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="655a1-102">SYNOPSIS</span></span>
<span data-ttu-id="655a1-103">Microsoft와 제휴 하는 피어 링 서비스 공급자의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="655a1-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="655a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="655a1-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="655a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="655a1-105">DESCRIPTION</span></span>
<span data-ttu-id="655a1-106">피어 링 서비스 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="655a1-106">List peering service providers</span></span>

## <span data-ttu-id="655a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="655a1-107">EXAMPLES</span></span>

### <span data-ttu-id="655a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="655a1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="655a1-109">사용 가능한 피어 링 서비스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="655a1-109">Gets available peering service providers</span></span>

## <span data-ttu-id="655a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="655a1-110">PARAMETERS</span></span>

### <span data-ttu-id="655a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655a1-111">-DefaultProfile</span></span>
<span data-ttu-id="655a1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="655a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="655a1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655a1-113">CommonParameters</span></span>
<span data-ttu-id="655a1-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="655a1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655a1-115">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="655a1-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655a1-116">입력</span><span class="sxs-lookup"><span data-stu-id="655a1-116">INPUTS</span></span>

### <span data-ttu-id="655a1-117">않아야</span><span class="sxs-lookup"><span data-stu-id="655a1-117">None</span></span>

## <span data-ttu-id="655a1-118">출력</span><span class="sxs-lookup"><span data-stu-id="655a1-118">OUTPUTS</span></span>

### <span data-ttu-id="655a1-119">PSPeeringServiceProvider (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="655a1-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="655a1-120">상속자</span><span class="sxs-lookup"><span data-stu-id="655a1-120">NOTES</span></span>

## <span data-ttu-id="655a1-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="655a1-121">RELATED LINKS</span></span>
