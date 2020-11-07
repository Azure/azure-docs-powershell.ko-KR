---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882185"
---
# <span data-ttu-id="211c2-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="211c2-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="211c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="211c2-102">SYNOPSIS</span></span>
<span data-ttu-id="211c2-103">가상 네트워크 게이트웨이를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="211c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="211c2-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="211c2-105">DESCRIPTION</span></span>
<span data-ttu-id="211c2-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="211c2-107">**AzureRmVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="211c2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="211c2-108">EXAMPLES</span></span>

### <span data-ttu-id="211c2-109">1: 가상 네트워크 게이트웨이 삭제</span><span class="sxs-lookup"><span data-stu-id="211c2-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="211c2-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이의 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="211c2-111">참고: 먼저 **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet을 사용 하 여 가상 네트워크 게이트웨이에 대 한 모든 연결을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="211c2-112">변수</span><span class="sxs-lookup"><span data-stu-id="211c2-112">PARAMETERS</span></span>

### <span data-ttu-id="211c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="211c2-113">-AsJob</span></span>
<span data-ttu-id="211c2-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="211c2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="211c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211c2-115">-DefaultProfile</span></span>
<span data-ttu-id="211c2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211c2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="211c2-117">-Force</span></span>
<span data-ttu-id="211c2-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="211c2-119">-이름</span><span class="sxs-lookup"><span data-stu-id="211c2-119">-Name</span></span>
<span data-ttu-id="211c2-120">이 cmdlet이 제거 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="211c2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="211c2-121">-PassThru</span></span>
<span data-ttu-id="211c2-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="211c2-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="211c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="211c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="211c2-125">가상 네트워크 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="211c2-126">-확인</span><span class="sxs-lookup"><span data-stu-id="211c2-126">-Confirm</span></span>
<span data-ttu-id="211c2-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211c2-128">-WhatIf</span></span>
<span data-ttu-id="211c2-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="211c2-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="211c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211c2-131">CommonParameters</span></span>
<span data-ttu-id="211c2-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="211c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211c2-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="211c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211c2-134">입력</span><span class="sxs-lookup"><span data-stu-id="211c2-134">INPUTS</span></span>

## <span data-ttu-id="211c2-135">출력</span><span class="sxs-lookup"><span data-stu-id="211c2-135">OUTPUTS</span></span>

## <span data-ttu-id="211c2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="211c2-136">NOTES</span></span>

## <span data-ttu-id="211c2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="211c2-137">RELATED LINKS</span></span>

