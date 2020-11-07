---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875438"
---
# <span data-ttu-id="619ac-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="619ac-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="619ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="619ac-102">SYNOPSIS</span></span>
<span data-ttu-id="619ac-103">부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="619ac-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="619ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="619ac-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="619ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="619ac-105">DESCRIPTION</span></span>
<span data-ttu-id="619ac-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="619ac-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="619ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="619ac-107">EXAMPLES</span></span>

### <span data-ttu-id="619ac-108">예제 1: 부하 분산 장치에 대 한 백 엔드 주소 풀 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="619ac-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="619ac-109">이 명령은 부하 분산 장치에 대 한 BackendAddressPool02 이라는 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="619ac-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="619ac-110">변수</span><span class="sxs-lookup"><span data-stu-id="619ac-110">PARAMETERS</span></span>

### <span data-ttu-id="619ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619ac-111">-DefaultProfile</span></span>
<span data-ttu-id="619ac-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="619ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="619ac-113">-이름</span><span class="sxs-lookup"><span data-stu-id="619ac-113">-Name</span></span>
<span data-ttu-id="619ac-114">만들려는 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="619ac-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="619ac-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619ac-115">CommonParameters</span></span>
<span data-ttu-id="619ac-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="619ac-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619ac-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="619ac-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619ac-118">입력</span><span class="sxs-lookup"><span data-stu-id="619ac-118">INPUTS</span></span>

## <span data-ttu-id="619ac-119">출력</span><span class="sxs-lookup"><span data-stu-id="619ac-119">OUTPUTS</span></span>

### <span data-ttu-id="619ac-120">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="619ac-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="619ac-121">상속자</span><span class="sxs-lookup"><span data-stu-id="619ac-121">NOTES</span></span>

## <span data-ttu-id="619ac-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="619ac-122">RELATED LINKS</span></span>

[<span data-ttu-id="619ac-123">추가-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="619ac-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="619ac-124">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="619ac-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="619ac-125">제거-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="619ac-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


