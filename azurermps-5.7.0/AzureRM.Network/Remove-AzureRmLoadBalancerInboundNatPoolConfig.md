---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: fd2a38a7b17e32a12cda0de7b5b620cffef9dfa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528023"
---
# <span data-ttu-id="52519-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="52519-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="52519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52519-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52519-103">구문과</span><span class="sxs-lookup"><span data-stu-id="52519-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52519-104">설명은</span><span class="sxs-lookup"><span data-stu-id="52519-104">DESCRIPTION</span></span>

## <span data-ttu-id="52519-105">예제의</span><span class="sxs-lookup"><span data-stu-id="52519-105">EXAMPLES</span></span>

### <span data-ttu-id="52519-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="52519-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="52519-107">변수</span><span class="sxs-lookup"><span data-stu-id="52519-107">PARAMETERS</span></span>

### <span data-ttu-id="52519-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52519-108">-DefaultProfile</span></span>
<span data-ttu-id="52519-109">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52519-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52519-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52519-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="52519-111">-이름</span><span class="sxs-lookup"><span data-stu-id="52519-111">-Name</span></span>
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

### <span data-ttu-id="52519-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52519-112">CommonParameters</span></span>
<span data-ttu-id="52519-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52519-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52519-114">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52519-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52519-115">입력</span><span class="sxs-lookup"><span data-stu-id="52519-115">INPUTS</span></span>

### <span data-ttu-id="52519-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52519-116">PSLoadBalancer</span></span>
<span data-ttu-id="52519-117">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="52519-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="52519-118">출력</span><span class="sxs-lookup"><span data-stu-id="52519-118">OUTPUTS</span></span>

### <span data-ttu-id="52519-119">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52519-119">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="52519-120">상속자</span><span class="sxs-lookup"><span data-stu-id="52519-120">NOTES</span></span>

## <span data-ttu-id="52519-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52519-121">RELATED LINKS</span></span>

