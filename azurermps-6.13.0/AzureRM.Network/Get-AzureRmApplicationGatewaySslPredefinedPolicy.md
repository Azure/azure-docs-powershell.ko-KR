---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 82713c41d6f2e3882c50ffbd5ab6b276a90dc2e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533372"
---
# <span data-ttu-id="ecbca-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="ecbca-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="ecbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecbca-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbca-103">응용 프로그램 게이트웨이에서 제공 하는 미리 정의 된 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecbca-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecbca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecbca-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecbca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecbca-105">DESCRIPTION</span></span>
<span data-ttu-id="ecbca-106">**AzureRmApplicationGatewaySslPredefinedPolicy** Cmdlet은 응용 프로그램 게이트웨이에서 제공 하는 미리 정의 된 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecbca-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="ecbca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ecbca-107">EXAMPLES</span></span>

### <span data-ttu-id="ecbca-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecbca-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="ecbca-109">이 명령은 미리 정의 된 모든 SSL 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecbca-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="ecbca-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="ecbca-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="ecbca-111">이 명령은 이름이 AppGwSslPolicy20170401 인 미리 정의 된 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecbca-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="ecbca-112">변수</span><span class="sxs-lookup"><span data-stu-id="ecbca-112">PARAMETERS</span></span>

### <span data-ttu-id="ecbca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbca-113">-DefaultProfile</span></span>
<span data-ttu-id="ecbca-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecbca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbca-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ecbca-115">-Name</span></span>
<span data-ttu-id="ecbca-116">Ssl 미리 정의 된 정책 이름</span><span class="sxs-lookup"><span data-stu-id="ecbca-116">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbca-117">CommonParameters</span></span>
<span data-ttu-id="ecbca-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecbca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbca-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecbca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbca-120">입력</span><span class="sxs-lookup"><span data-stu-id="ecbca-120">INPUTS</span></span>

### <span data-ttu-id="ecbca-121">않아야</span><span class="sxs-lookup"><span data-stu-id="ecbca-121">None</span></span>

## <span data-ttu-id="ecbca-122">출력</span><span class="sxs-lookup"><span data-stu-id="ecbca-122">OUTPUTS</span></span>

### <span data-ttu-id="ecbca-123">PSApplicationGatewaySslPredefinedPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ecbca-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="ecbca-124">상속자</span><span class="sxs-lookup"><span data-stu-id="ecbca-124">NOTES</span></span>

## <span data-ttu-id="ecbca-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecbca-125">RELATED LINKS</span></span>
