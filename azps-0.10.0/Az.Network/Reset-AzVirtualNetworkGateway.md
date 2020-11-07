---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876627"
---
# <span data-ttu-id="211a3-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="211a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="211a3-102">SYNOPSIS</span></span>

## <span data-ttu-id="211a3-103">구문과</span><span class="sxs-lookup"><span data-stu-id="211a3-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="211a3-104">설명은</span><span class="sxs-lookup"><span data-stu-id="211a3-104">DESCRIPTION</span></span>

## <span data-ttu-id="211a3-105">예제의</span><span class="sxs-lookup"><span data-stu-id="211a3-105">EXAMPLES</span></span>

### <span data-ttu-id="211a3-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="211a3-106">1:</span></span>
```

```

## <span data-ttu-id="211a3-107">변수</span><span class="sxs-lookup"><span data-stu-id="211a3-107">PARAMETERS</span></span>

### <span data-ttu-id="211a3-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="211a3-108">-AsJob</span></span>
<span data-ttu-id="211a3-109">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="211a3-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="211a3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211a3-110">-DefaultProfile</span></span>
<span data-ttu-id="211a3-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="211a3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211a3-112">-게이트웨이 Vip</span><span class="sxs-lookup"><span data-stu-id="211a3-112">-GatewayVip</span></span>
<span data-ttu-id="211a3-113">특정 게이트웨이 인스턴스를 다시 설정 하기 위한 게이트웨이 vip (예: Active-Active 기능을 사용할 수 있는 게이트웨이를 사용 하는 경우) 값이 전달 되지 않으면 기본적으로 게이트웨이 기본 인스턴스가 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="211a3-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="211a3-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="211a3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211a3-115">CommonParameters</span></span>
<span data-ttu-id="211a3-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="211a3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211a3-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="211a3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211a3-118">입력</span><span class="sxs-lookup"><span data-stu-id="211a3-118">INPUTS</span></span>

### <span data-ttu-id="211a3-119">이름</span><span class="sxs-lookup"><span data-stu-id="211a3-119">String</span></span>
<span data-ttu-id="211a3-120">'. H i m ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="211a3-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="211a3-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="211a3-122">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="211a3-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="211a3-123">출력</span><span class="sxs-lookup"><span data-stu-id="211a3-123">OUTPUTS</span></span>

### <span data-ttu-id="211a3-124">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="211a3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="211a3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="211a3-125">NOTES</span></span>

## <span data-ttu-id="211a3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="211a3-126">RELATED LINKS</span></span>

[<span data-ttu-id="211a3-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="211a3-128">새로운 AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="211a3-129">제거-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="211a3-130">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="211a3-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211a3-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


