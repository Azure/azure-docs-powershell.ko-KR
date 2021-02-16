---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189713"
---
# <span data-ttu-id="90a5a-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="90a5a-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="90a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="90a5a-103">연결에 사용되는 공유 키를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90a5a-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="90a5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="90a5a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90a5a-105">설명</span><span class="sxs-lookup"><span data-stu-id="90a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="90a5a-106">연결에 사용되는 공유 키를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90a5a-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="90a5a-107">예제</span><span class="sxs-lookup"><span data-stu-id="90a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="90a5a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="90a5a-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="90a5a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90a5a-109">PARAMETERS</span></span>

### <span data-ttu-id="90a5a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a5a-110">-DefaultProfile</span></span>
<span data-ttu-id="90a5a-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90a5a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a5a-112">-Name</span><span class="sxs-lookup"><span data-stu-id="90a5a-112">-Name</span></span>
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

### <span data-ttu-id="90a5a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a5a-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="90a5a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a5a-114">CommonParameters</span></span>
<span data-ttu-id="90a5a-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90a5a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a5a-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90a5a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a5a-117">입력</span><span class="sxs-lookup"><span data-stu-id="90a5a-117">INPUTS</span></span>

### <span data-ttu-id="90a5a-118">System.String</span><span class="sxs-lookup"><span data-stu-id="90a5a-118">System.String</span></span>

## <span data-ttu-id="90a5a-119">출력</span><span class="sxs-lookup"><span data-stu-id="90a5a-119">OUTPUTS</span></span>

### <span data-ttu-id="90a5a-120">System.String</span><span class="sxs-lookup"><span data-stu-id="90a5a-120">System.String</span></span>

## <span data-ttu-id="90a5a-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90a5a-121">NOTES</span></span>

## <span data-ttu-id="90a5a-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90a5a-122">RELATED LINKS</span></span>

[<span data-ttu-id="90a5a-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="90a5a-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="90a5a-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="90a5a-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
