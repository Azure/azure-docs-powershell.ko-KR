---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: f3268d78ac0630e18307646086689cb8d435c290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702913"
---
# <span data-ttu-id="6da42-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6da42-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="6da42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6da42-102">SYNOPSIS</span></span>
<span data-ttu-id="6da42-103">가상 네트워크 게이트웨이 연결의 공유 키를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6da42-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6da42-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6da42-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6da42-105">DESCRIPTION</span></span>
<span data-ttu-id="6da42-106">**Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet은 가상 네트워크 게이트웨이 연결의 공유 키를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="6da42-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6da42-107">EXAMPLES</span></span>

### <span data-ttu-id="6da42-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="6da42-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="6da42-109">변수</span><span class="sxs-lookup"><span data-stu-id="6da42-109">PARAMETERS</span></span>

### <span data-ttu-id="6da42-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da42-110">-DefaultProfile</span></span>
<span data-ttu-id="6da42-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da42-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6da42-112">-Force</span></span>
<span data-ttu-id="6da42-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da42-114">-이름</span><span class="sxs-lookup"><span data-stu-id="6da42-114">-Name</span></span>
<span data-ttu-id="6da42-115">가상 네트워크 게이트웨이 공유 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da42-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da42-116">-ResourceGroupName</span></span>
<span data-ttu-id="6da42-117">가상 네트워크 게이트웨이가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="6da42-118">-값</span><span class="sxs-lookup"><span data-stu-id="6da42-118">-Value</span></span>
<span data-ttu-id="6da42-119">공유 키의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="6da42-120">-확인</span><span class="sxs-lookup"><span data-stu-id="6da42-120">-Confirm</span></span>
<span data-ttu-id="6da42-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da42-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da42-122">-WhatIf</span></span>
<span data-ttu-id="6da42-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da42-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da42-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da42-125">CommonParameters</span></span>
<span data-ttu-id="6da42-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da42-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da42-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da42-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da42-128">입력</span><span class="sxs-lookup"><span data-stu-id="6da42-128">INPUTS</span></span>

### <span data-ttu-id="6da42-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6da42-129">System.String</span></span>

## <span data-ttu-id="6da42-130">출력</span><span class="sxs-lookup"><span data-stu-id="6da42-130">OUTPUTS</span></span>

### <span data-ttu-id="6da42-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6da42-131">System.String</span></span>

## <span data-ttu-id="6da42-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6da42-132">NOTES</span></span>

## <span data-ttu-id="6da42-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6da42-133">RELATED LINKS</span></span>

[<span data-ttu-id="6da42-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6da42-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="6da42-135">다시 설정-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6da42-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


