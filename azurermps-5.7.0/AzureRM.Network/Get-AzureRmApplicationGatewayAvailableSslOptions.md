---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 091170e4cea82184369b3c10c7fd71cb2d326244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531031"
---
# <span data-ttu-id="16c04-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="16c04-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="16c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c04-102">SYNOPSIS</span></span>
<span data-ttu-id="16c04-103">응용 프로그램 게이트웨이의 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16c04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16c04-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16c04-105">DESCRIPTION</span></span>
<span data-ttu-id="16c04-106">**AzureRmApplicationGatewayAvailableSslOptions** cmdlet은 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="16c04-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16c04-107">EXAMPLES</span></span>

### <span data-ttu-id="16c04-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="16c04-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="16c04-109">이 명령은 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="16c04-110">변수</span><span class="sxs-lookup"><span data-stu-id="16c04-110">PARAMETERS</span></span>

### <span data-ttu-id="16c04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c04-111">-DefaultProfile</span></span>
<span data-ttu-id="16c04-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c04-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c04-113">CommonParameters</span></span>
<span data-ttu-id="16c04-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c04-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c04-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c04-116">입력</span><span class="sxs-lookup"><span data-stu-id="16c04-116">INPUTS</span></span>

### <span data-ttu-id="16c04-117">않아야</span><span class="sxs-lookup"><span data-stu-id="16c04-117">None</span></span>

## <span data-ttu-id="16c04-118">출력</span><span class="sxs-lookup"><span data-stu-id="16c04-118">OUTPUTS</span></span>

### <span data-ttu-id="16c04-119">PSApplicationGatewayAvailableSslOptions에 대 한.</span><span class="sxs-lookup"><span data-stu-id="16c04-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="16c04-120">상속자</span><span class="sxs-lookup"><span data-stu-id="16c04-120">NOTES</span></span>

## <span data-ttu-id="16c04-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16c04-121">RELATED LINKS</span></span>

