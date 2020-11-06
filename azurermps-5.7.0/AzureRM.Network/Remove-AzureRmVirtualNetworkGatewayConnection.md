---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 73bb12aebbe4f67c1aba4526f6ed656e5b6feb09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535300"
---
# <span data-ttu-id="66c63-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="66c63-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="66c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c63-102">SYNOPSIS</span></span>
<span data-ttu-id="66c63-103">가상 네트워크 게이트웨이 연결을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66c63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66c63-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66c63-105">DESCRIPTION</span></span>
<span data-ttu-id="66c63-106">가상 네트워크 게이트웨이 연결은 Azure의 가상 네트워크 게이트웨이에 연결 된 IPsec 터널 (사이트 간 또는 Vnet to Vnet)을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="66c63-107">**AzureRmVirtualNetworkGatewayConnection** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 연결 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="66c63-108">예제의</span><span class="sxs-lookup"><span data-stu-id="66c63-108">EXAMPLES</span></span>

### <span data-ttu-id="66c63-109">1: 가상 네트워크 게이트웨이 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="66c63-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="66c63-110">리소스 그룹 "Mytunnel" 내에서 이름이 "myTunnel" 인 가상 네트워크 게이트웨이 연결의 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="66c63-111">변수</span><span class="sxs-lookup"><span data-stu-id="66c63-111">PARAMETERS</span></span>

### <span data-ttu-id="66c63-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c63-112">-DefaultProfile</span></span>
<span data-ttu-id="66c63-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c63-114">-Force</span><span class="sxs-lookup"><span data-stu-id="66c63-114">-Force</span></span>
<span data-ttu-id="66c63-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66c63-116">-이름</span><span class="sxs-lookup"><span data-stu-id="66c63-116">-Name</span></span>
<span data-ttu-id="66c63-117">이 cmdlet이 제거 하는 가상 네트워크 게이트웨이 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66c63-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66c63-118">-PassThru</span></span>
<span data-ttu-id="66c63-119">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66c63-120">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66c63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c63-121">-ResourceGroupName</span></span>
<span data-ttu-id="66c63-122">가상 네트워크 게이트웨이 연결을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="66c63-123">-확인</span><span class="sxs-lookup"><span data-stu-id="66c63-123">-Confirm</span></span>
<span data-ttu-id="66c63-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c63-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c63-125">-WhatIf</span></span>
<span data-ttu-id="66c63-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c63-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c63-128">CommonParameters</span></span>
<span data-ttu-id="66c63-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c63-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c63-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c63-131">입력</span><span class="sxs-lookup"><span data-stu-id="66c63-131">INPUTS</span></span>

### <span data-ttu-id="66c63-132">않아야</span><span class="sxs-lookup"><span data-stu-id="66c63-132">None</span></span>
<span data-ttu-id="66c63-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c63-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66c63-134">출력</span><span class="sxs-lookup"><span data-stu-id="66c63-134">OUTPUTS</span></span>

## <span data-ttu-id="66c63-135">상속자</span><span class="sxs-lookup"><span data-stu-id="66c63-135">NOTES</span></span>

## <span data-ttu-id="66c63-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66c63-136">RELATED LINKS</span></span>

[<span data-ttu-id="66c63-137">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="66c63-137">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="66c63-138">새로운 AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="66c63-138">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="66c63-139">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="66c63-139">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


