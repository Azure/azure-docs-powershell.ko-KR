---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 945f1d8d12b4a493ca361c04ae14cd899f91956f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711415"
---
# <span data-ttu-id="050ce-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="050ce-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="050ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050ce-102">SYNOPSIS</span></span>
<span data-ttu-id="050ce-103">가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="050ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="050ce-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="050ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="050ce-105">DESCRIPTION</span></span>
<span data-ttu-id="050ce-106">**AzureRmVirtualNetwork** Cmdlet은 Azure 가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="050ce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="050ce-107">EXAMPLES</span></span>

### <span data-ttu-id="050ce-108">1: 가상 네트워크 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="050ce-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="050ce-109">이 예제에서는 리소스 그룹에 가상 네트워크를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="050ce-110">가상 네트워크를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="050ce-111">변수</span><span class="sxs-lookup"><span data-stu-id="050ce-111">PARAMETERS</span></span>

### <span data-ttu-id="050ce-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="050ce-112">-AsJob</span></span>
<span data-ttu-id="050ce-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="050ce-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="050ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050ce-114">-DefaultProfile</span></span>
<span data-ttu-id="050ce-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="050ce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="050ce-116">-Force</span></span>
<span data-ttu-id="050ce-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="050ce-118">-이름</span><span class="sxs-lookup"><span data-stu-id="050ce-118">-Name</span></span>
<span data-ttu-id="050ce-119">이 cmdlet이 제거 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="050ce-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="050ce-120">-PassThru</span></span>
<span data-ttu-id="050ce-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="050ce-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="050ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="050ce-124">이 cmdlet이 제거 하는 가상 네트워크를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="050ce-125">-확인</span><span class="sxs-lookup"><span data-stu-id="050ce-125">-Confirm</span></span>
<span data-ttu-id="050ce-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050ce-127">-WhatIf</span></span>
<span data-ttu-id="050ce-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="050ce-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050ce-130">CommonParameters</span></span>
<span data-ttu-id="050ce-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050ce-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="050ce-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050ce-133">입력</span><span class="sxs-lookup"><span data-stu-id="050ce-133">INPUTS</span></span>

### <span data-ttu-id="050ce-134">않아야</span><span class="sxs-lookup"><span data-stu-id="050ce-134">None</span></span>
<span data-ttu-id="050ce-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="050ce-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="050ce-136">출력</span><span class="sxs-lookup"><span data-stu-id="050ce-136">OUTPUTS</span></span>

## <span data-ttu-id="050ce-137">상속자</span><span class="sxs-lookup"><span data-stu-id="050ce-137">NOTES</span></span>

## <span data-ttu-id="050ce-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="050ce-138">RELATED LINKS</span></span>

[<span data-ttu-id="050ce-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="050ce-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="050ce-140">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="050ce-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="050ce-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="050ce-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


