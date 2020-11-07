---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702925"
---
# <span data-ttu-id="dc0c8-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="dc0c8-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="dc0c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0c8-103">연결에 사용 된 공유 키를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc0c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc0c8-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc0c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc0c8-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0c8-106">연결에 사용 된 공유 키를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="dc0c8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dc0c8-107">EXAMPLES</span></span>

### <span data-ttu-id="dc0c8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc0c8-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="dc0c8-109">변수</span><span class="sxs-lookup"><span data-stu-id="dc0c8-109">PARAMETERS</span></span>

### <span data-ttu-id="dc0c8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0c8-110">-DefaultProfile</span></span>
<span data-ttu-id="dc0c8-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc0c8-112">-이름</span><span class="sxs-lookup"><span data-stu-id="dc0c8-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0c8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0c8-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0c8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0c8-114">CommonParameters</span></span>
<span data-ttu-id="dc0c8-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0c8-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc0c8-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0c8-117">입력</span><span class="sxs-lookup"><span data-stu-id="dc0c8-117">INPUTS</span></span>

### <span data-ttu-id="dc0c8-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc0c8-118">System.String</span></span>

## <span data-ttu-id="dc0c8-119">출력</span><span class="sxs-lookup"><span data-stu-id="dc0c8-119">OUTPUTS</span></span>

### <span data-ttu-id="dc0c8-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc0c8-120">System.String</span></span>

## <span data-ttu-id="dc0c8-121">상속자</span><span class="sxs-lookup"><span data-stu-id="dc0c8-121">NOTES</span></span>

## <span data-ttu-id="dc0c8-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc0c8-122">RELATED LINKS</span></span>
