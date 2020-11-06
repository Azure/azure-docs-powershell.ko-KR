---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537703"
---
# <span data-ttu-id="66c2c-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="66c2c-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="66c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="66c2c-103">로컬 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66c2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66c2c-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c2c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="66c2c-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="66c2c-107">**AzureRmLocalNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 온-프레미스 gateway를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="66c2c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="66c2c-108">EXAMPLES</span></span>

### <span data-ttu-id="66c2c-109">1: 로컬 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="66c2c-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="66c2c-110">리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="66c2c-111">변수</span><span class="sxs-lookup"><span data-stu-id="66c2c-111">PARAMETERS</span></span>

### <span data-ttu-id="66c2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c2c-112">-DefaultProfile</span></span>
<span data-ttu-id="66c2c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c2c-114">-이름</span><span class="sxs-lookup"><span data-stu-id="66c2c-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c2c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c2c-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c2c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c2c-116">CommonParameters</span></span>
<span data-ttu-id="66c2c-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c2c-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c2c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c2c-119">입력</span><span class="sxs-lookup"><span data-stu-id="66c2c-119">INPUTS</span></span>

### <span data-ttu-id="66c2c-120">않아야</span><span class="sxs-lookup"><span data-stu-id="66c2c-120">None</span></span>
<span data-ttu-id="66c2c-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c2c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66c2c-122">출력</span><span class="sxs-lookup"><span data-stu-id="66c2c-122">OUTPUTS</span></span>

### <span data-ttu-id="66c2c-123">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="66c2c-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="66c2c-124">상속자</span><span class="sxs-lookup"><span data-stu-id="66c2c-124">NOTES</span></span>

## <span data-ttu-id="66c2c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66c2c-125">RELATED LINKS</span></span>

