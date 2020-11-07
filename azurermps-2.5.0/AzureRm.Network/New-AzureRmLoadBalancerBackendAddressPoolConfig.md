---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 367e5d74b9d2c1d29199a7af3c132e147b5ae620
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881365"
---
# <span data-ttu-id="73766-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73766-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="73766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73766-102">SYNOPSIS</span></span>
<span data-ttu-id="73766-103">부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73766-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73766-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73766-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73766-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73766-105">DESCRIPTION</span></span>
<span data-ttu-id="73766-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73766-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="73766-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73766-107">EXAMPLES</span></span>

### <span data-ttu-id="73766-108">예제 1: 부하 분산 장치에 대 한 백 엔드 주소 풀 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="73766-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="73766-109">이 명령은 부하 분산 장치에 대 한 BackendAddressPool02 이라는 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73766-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="73766-110">변수</span><span class="sxs-lookup"><span data-stu-id="73766-110">PARAMETERS</span></span>

### <span data-ttu-id="73766-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73766-111">-DefaultProfile</span></span>
<span data-ttu-id="73766-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73766-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73766-113">-이름</span><span class="sxs-lookup"><span data-stu-id="73766-113">-Name</span></span>
<span data-ttu-id="73766-114">만들려는 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73766-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73766-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73766-115">CommonParameters</span></span>
<span data-ttu-id="73766-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73766-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73766-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73766-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73766-118">입력</span><span class="sxs-lookup"><span data-stu-id="73766-118">INPUTS</span></span>

## <span data-ttu-id="73766-119">출력</span><span class="sxs-lookup"><span data-stu-id="73766-119">OUTPUTS</span></span>

### <span data-ttu-id="73766-120">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="73766-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="73766-121">상속자</span><span class="sxs-lookup"><span data-stu-id="73766-121">NOTES</span></span>

## <span data-ttu-id="73766-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73766-122">RELATED LINKS</span></span>

[<span data-ttu-id="73766-123">추가-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73766-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="73766-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73766-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="73766-125">제거-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73766-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


