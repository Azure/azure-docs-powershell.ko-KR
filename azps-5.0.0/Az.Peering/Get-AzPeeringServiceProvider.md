---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217574"
---
# <span data-ttu-id="e651a-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="e651a-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="e651a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e651a-102">SYNOPSIS</span></span>
<span data-ttu-id="e651a-103">Microsoft와 제휴 하는 피어 링 서비스 공급자의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e651a-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="e651a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e651a-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e651a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e651a-105">DESCRIPTION</span></span>
<span data-ttu-id="e651a-106">피어 링 서비스 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="e651a-106">List peering service providers</span></span>

## <span data-ttu-id="e651a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e651a-107">EXAMPLES</span></span>

### <span data-ttu-id="e651a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e651a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="e651a-109">사용 가능한 피어 링 서비스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e651a-109">Gets available peering service providers</span></span>

## <span data-ttu-id="e651a-110">변수</span><span class="sxs-lookup"><span data-stu-id="e651a-110">PARAMETERS</span></span>

### <span data-ttu-id="e651a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e651a-111">-DefaultProfile</span></span>
<span data-ttu-id="e651a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e651a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e651a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e651a-113">CommonParameters</span></span>
<span data-ttu-id="e651a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e651a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e651a-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e651a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e651a-116">입력</span><span class="sxs-lookup"><span data-stu-id="e651a-116">INPUTS</span></span>

### <span data-ttu-id="e651a-117">않아야</span><span class="sxs-lookup"><span data-stu-id="e651a-117">None</span></span>

## <span data-ttu-id="e651a-118">출력</span><span class="sxs-lookup"><span data-stu-id="e651a-118">OUTPUTS</span></span>

### <span data-ttu-id="e651a-119">PSPeeringServiceProvider (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e651a-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="e651a-120">상속자</span><span class="sxs-lookup"><span data-stu-id="e651a-120">NOTES</span></span>

## <span data-ttu-id="e651a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e651a-121">RELATED LINKS</span></span>
