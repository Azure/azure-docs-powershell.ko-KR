---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 14a77eeaeb502c79663f9d95cbff3ffc199ddc67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974811"
---
# <span data-ttu-id="fc175-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fc175-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="fc175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc175-102">SYNOPSIS</span></span>
<span data-ttu-id="fc175-103">연결에 사용되는 공유 키를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fc175-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="fc175-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc175-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc175-105">설명</span><span class="sxs-lookup"><span data-stu-id="fc175-105">DESCRIPTION</span></span>
<span data-ttu-id="fc175-106">연결에 사용되는 공유 키를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fc175-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="fc175-107">예제</span><span class="sxs-lookup"><span data-stu-id="fc175-107">EXAMPLES</span></span>

### <span data-ttu-id="fc175-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc175-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="fc175-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc175-109">PARAMETERS</span></span>

### <span data-ttu-id="fc175-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc175-110">-DefaultProfile</span></span>
<span data-ttu-id="fc175-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc175-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc175-112">-Name</span><span class="sxs-lookup"><span data-stu-id="fc175-112">-Name</span></span>
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

### <span data-ttu-id="fc175-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc175-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fc175-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc175-114">CommonParameters</span></span>
<span data-ttu-id="fc175-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc175-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc175-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc175-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc175-117">입력</span><span class="sxs-lookup"><span data-stu-id="fc175-117">INPUTS</span></span>

### <span data-ttu-id="fc175-118">System.String</span><span class="sxs-lookup"><span data-stu-id="fc175-118">System.String</span></span>

## <span data-ttu-id="fc175-119">출력</span><span class="sxs-lookup"><span data-stu-id="fc175-119">OUTPUTS</span></span>

### <span data-ttu-id="fc175-120">System.String</span><span class="sxs-lookup"><span data-stu-id="fc175-120">System.String</span></span>

## <span data-ttu-id="fc175-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc175-121">NOTES</span></span>

## <span data-ttu-id="fc175-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc175-122">RELATED LINKS</span></span>

[<span data-ttu-id="fc175-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fc175-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="fc175-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fc175-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
