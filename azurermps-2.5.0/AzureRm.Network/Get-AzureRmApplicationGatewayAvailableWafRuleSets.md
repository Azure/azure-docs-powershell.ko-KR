---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881482"
---
# <span data-ttu-id="6cd66-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="6cd66-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="6cd66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd66-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd66-103">사용할 수 있는 모든 웹 응용 프로그램 방화벽 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cd66-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cd66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cd66-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cd66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6cd66-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd66-106">**AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet은 사용 가능한 모든 웹 응용 프로그램 방화벽 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cd66-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="6cd66-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6cd66-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd66-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6cd66-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="6cd66-109">이 명령은 사용 가능한 모든 웹 응용 프로그램 방화벽 규칙 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cd66-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="6cd66-110">변수</span><span class="sxs-lookup"><span data-stu-id="6cd66-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd66-111">-DefaultProfile</span></span>
<span data-ttu-id="6cd66-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cd66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd66-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd66-113">CommonParameters</span></span>
<span data-ttu-id="6cd66-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cd66-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd66-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd66-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd66-116">입력</span><span class="sxs-lookup"><span data-stu-id="6cd66-116">INPUTS</span></span>

### <span data-ttu-id="6cd66-117">않아야</span><span class="sxs-lookup"><span data-stu-id="6cd66-117">None</span></span>

## <span data-ttu-id="6cd66-118">출력</span><span class="sxs-lookup"><span data-stu-id="6cd66-118">OUTPUTS</span></span>

### <span data-ttu-id="6cd66-119">PSApplicationGatewayAvailableWafRuleSetsResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6cd66-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="6cd66-120">상속자</span><span class="sxs-lookup"><span data-stu-id="6cd66-120">NOTES</span></span>
<span data-ttu-id="6cd66-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** 는 **AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet에 대 한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="6cd66-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="6cd66-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cd66-122">RELATED LINKS</span></span>

