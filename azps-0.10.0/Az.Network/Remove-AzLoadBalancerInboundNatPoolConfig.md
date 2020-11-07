---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 2486dadb4d1987a2a3c341bc9f66270ec1338a1b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875333"
---
# <span data-ttu-id="b67a6-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b67a6-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b67a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b67a6-102">SYNOPSIS</span></span>

## <span data-ttu-id="b67a6-103">구문과</span><span class="sxs-lookup"><span data-stu-id="b67a6-103">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b67a6-104">설명은</span><span class="sxs-lookup"><span data-stu-id="b67a6-104">DESCRIPTION</span></span>

## <span data-ttu-id="b67a6-105">예제의</span><span class="sxs-lookup"><span data-stu-id="b67a6-105">EXAMPLES</span></span>

### <span data-ttu-id="b67a6-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="b67a6-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b67a6-107">변수</span><span class="sxs-lookup"><span data-stu-id="b67a6-107">PARAMETERS</span></span>

### <span data-ttu-id="b67a6-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67a6-108">-DefaultProfile</span></span>
<span data-ttu-id="b67a6-109">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b67a6-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b67a6-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67a6-110">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67a6-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b67a6-111">-Name</span></span>
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

### <span data-ttu-id="b67a6-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67a6-112">CommonParameters</span></span>
<span data-ttu-id="b67a6-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b67a6-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67a6-114">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b67a6-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67a6-115">입력</span><span class="sxs-lookup"><span data-stu-id="b67a6-115">INPUTS</span></span>

### <span data-ttu-id="b67a6-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67a6-116">PSLoadBalancer</span></span>
<span data-ttu-id="b67a6-117">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b67a6-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b67a6-118">출력</span><span class="sxs-lookup"><span data-stu-id="b67a6-118">OUTPUTS</span></span>

### <span data-ttu-id="b67a6-119">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67a6-119">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b67a6-120">상속자</span><span class="sxs-lookup"><span data-stu-id="b67a6-120">NOTES</span></span>

## <span data-ttu-id="b67a6-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b67a6-121">RELATED LINKS</span></span>

