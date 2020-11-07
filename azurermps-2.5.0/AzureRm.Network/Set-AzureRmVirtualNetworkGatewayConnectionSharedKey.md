---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882161"
---
# <span data-ttu-id="f3958-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f3958-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f3958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3958-102">SYNOPSIS</span></span>
<span data-ttu-id="f3958-103">가상 네트워크 게이트웨이 연결의 공유 키를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3958-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3958-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3958-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3958-105">DESCRIPTION</span></span>
<span data-ttu-id="f3958-106">**Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet은 가상 네트워크 게이트웨이 연결의 공유 키를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f3958-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3958-107">EXAMPLES</span></span>

### <span data-ttu-id="f3958-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="f3958-108">1:</span></span>
```

```

## <span data-ttu-id="f3958-109">변수</span><span class="sxs-lookup"><span data-stu-id="f3958-109">PARAMETERS</span></span>

### <span data-ttu-id="f3958-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3958-110">-DefaultProfile</span></span>
<span data-ttu-id="f3958-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3958-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f3958-112">-Force</span></span>
<span data-ttu-id="f3958-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3958-114">-이름</span><span class="sxs-lookup"><span data-stu-id="f3958-114">-Name</span></span>
<span data-ttu-id="f3958-115">가상 네트워크 게이트웨이 공유 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3958-116">-ResourceGroupName</span></span>
<span data-ttu-id="f3958-117">가상 네트워크 게이트웨이가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="f3958-118">-값</span><span class="sxs-lookup"><span data-stu-id="f3958-118">-Value</span></span>
<span data-ttu-id="f3958-119">공유 키의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="f3958-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f3958-120">-Confirm</span></span>
<span data-ttu-id="f3958-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3958-122">-WhatIf</span></span>
<span data-ttu-id="f3958-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3958-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3958-125">CommonParameters</span></span>
<span data-ttu-id="f3958-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3958-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3958-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3958-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3958-128">입력</span><span class="sxs-lookup"><span data-stu-id="f3958-128">INPUTS</span></span>

## <span data-ttu-id="f3958-129">출력</span><span class="sxs-lookup"><span data-stu-id="f3958-129">OUTPUTS</span></span>

### <span data-ttu-id="f3958-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3958-130">System.String</span></span>

## <span data-ttu-id="f3958-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f3958-131">NOTES</span></span>

## <span data-ttu-id="f3958-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3958-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3958-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f3958-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f3958-134">다시 설정-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f3958-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


