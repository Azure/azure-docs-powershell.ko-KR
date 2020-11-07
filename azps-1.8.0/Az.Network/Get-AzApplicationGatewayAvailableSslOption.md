---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 04a24ee5148782f4a15aa5b93ffb937ad312ccfb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700668"
---
# <span data-ttu-id="c813e-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="c813e-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="c813e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c813e-102">SYNOPSIS</span></span>
<span data-ttu-id="c813e-103">응용 프로그램 게이트웨이의 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c813e-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="c813e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c813e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c813e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c813e-105">DESCRIPTION</span></span>
<span data-ttu-id="c813e-106">**AzApplicationGatewayAvailableSslOption** cmdlet은 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c813e-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="c813e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c813e-107">EXAMPLES</span></span>

### <span data-ttu-id="c813e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c813e-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="c813e-109">이 명령은 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c813e-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="c813e-110">변수</span><span class="sxs-lookup"><span data-stu-id="c813e-110">PARAMETERS</span></span>

### <span data-ttu-id="c813e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c813e-111">-DefaultProfile</span></span>
<span data-ttu-id="c813e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c813e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c813e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c813e-113">CommonParameters</span></span>
<span data-ttu-id="c813e-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c813e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c813e-115">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c813e-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c813e-116">입력</span><span class="sxs-lookup"><span data-stu-id="c813e-116">INPUTS</span></span>

### <span data-ttu-id="c813e-117">않아야</span><span class="sxs-lookup"><span data-stu-id="c813e-117">None</span></span>

## <span data-ttu-id="c813e-118">출력</span><span class="sxs-lookup"><span data-stu-id="c813e-118">OUTPUTS</span></span>

### <span data-ttu-id="c813e-119">PSApplicationGatewayAvailableSslOptions에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c813e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="c813e-120">상속자</span><span class="sxs-lookup"><span data-stu-id="c813e-120">NOTES</span></span>

## <span data-ttu-id="c813e-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c813e-121">RELATED LINKS</span></span>