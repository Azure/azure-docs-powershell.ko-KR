---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
ms.openlocfilehash: a977de2b4a60f0fc5ae93e175d521d398d40f850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882966"
---
# <span data-ttu-id="2c400-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="2c400-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="2c400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c400-102">SYNOPSIS</span></span>
<span data-ttu-id="2c400-103">응용 프로그램 게이트웨이에서 제공 하는 미리 정의 된 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c400-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c400-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c400-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c400-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2c400-105">DESCRIPTION</span></span>
<span data-ttu-id="2c400-106">**AzureRmApplicationGatewaySslPredefinedPolicy** Cmdlet은 응용 프로그램 게이트웨이에서 제공 하는 미리 정의 된 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c400-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="2c400-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2c400-107">EXAMPLES</span></span>

### <span data-ttu-id="2c400-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c400-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="2c400-109">이 명령은 미리 정의 된 모든 SSL 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c400-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="2c400-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2c400-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="2c400-111">이 명령은 이름이 AppGwSslPolicy20170401 인 미리 정의 된 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c400-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="2c400-112">변수</span><span class="sxs-lookup"><span data-stu-id="2c400-112">PARAMETERS</span></span>

### <span data-ttu-id="2c400-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c400-113">-DefaultProfile</span></span>
<span data-ttu-id="2c400-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c400-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c400-115">-이름</span><span class="sxs-lookup"><span data-stu-id="2c400-115">-Name</span></span>
<span data-ttu-id="2c400-116">Ssl 미리 정의 된 정책 이름</span><span class="sxs-lookup"><span data-stu-id="2c400-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c400-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c400-117">CommonParameters</span></span>
<span data-ttu-id="2c400-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c400-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c400-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c400-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c400-120">입력</span><span class="sxs-lookup"><span data-stu-id="2c400-120">INPUTS</span></span>

### <span data-ttu-id="2c400-121">않아야</span><span class="sxs-lookup"><span data-stu-id="2c400-121">None</span></span>

## <span data-ttu-id="2c400-122">출력</span><span class="sxs-lookup"><span data-stu-id="2c400-122">OUTPUTS</span></span>

### <span data-ttu-id="2c400-123">PSApplicationGatewaySslPredefinedPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2c400-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="2c400-124">4.1.0.0, PSApplicationGatewaySslPredefinedPolicy, Microsoft azure. Commands. 네트워크, 버전 =, Culture = 중립, PublicKeyToken = null]],. 컬렉션인 ' 1 [[Microsoft azure.]</span><span class="sxs-lookup"><span data-stu-id="2c400-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2c400-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2c400-125">NOTES</span></span>

## <span data-ttu-id="2c400-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c400-126">RELATED LINKS</span></span>

