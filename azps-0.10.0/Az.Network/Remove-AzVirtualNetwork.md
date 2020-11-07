---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: b65fcbc132923f18c0a70187403e4c4ba2cef52a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876646"
---
# <span data-ttu-id="7daf8-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7daf8-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="7daf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7daf8-102">SYNOPSIS</span></span>
<span data-ttu-id="7daf8-103">가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-103">Removes a virtual network.</span></span>

## <span data-ttu-id="7daf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7daf8-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7daf8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7daf8-105">DESCRIPTION</span></span>
<span data-ttu-id="7daf8-106">**AzVirtualNetwork** Cmdlet은 Azure 가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="7daf8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7daf8-107">EXAMPLES</span></span>

### <span data-ttu-id="7daf8-108">1: 가상 네트워크 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="7daf8-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="7daf8-109">이 예제에서는 리소스 그룹에 가상 네트워크를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="7daf8-110">가상 네트워크를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="7daf8-111">변수</span><span class="sxs-lookup"><span data-stu-id="7daf8-111">PARAMETERS</span></span>

### <span data-ttu-id="7daf8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7daf8-112">-AsJob</span></span>
<span data-ttu-id="7daf8-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7daf8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7daf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7daf8-114">-DefaultProfile</span></span>
<span data-ttu-id="7daf8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7daf8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7daf8-116">-Force</span></span>
<span data-ttu-id="7daf8-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7daf8-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7daf8-118">-Name</span></span>
<span data-ttu-id="7daf8-119">이 cmdlet이 제거 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7daf8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7daf8-120">-PassThru</span></span>
<span data-ttu-id="7daf8-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7daf8-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7daf8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7daf8-123">-ResourceGroupName</span></span>
<span data-ttu-id="7daf8-124">이 cmdlet이 제거 하는 가상 네트워크를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7daf8-125">-확인</span><span class="sxs-lookup"><span data-stu-id="7daf8-125">-Confirm</span></span>
<span data-ttu-id="7daf8-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7daf8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7daf8-127">-WhatIf</span></span>
<span data-ttu-id="7daf8-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7daf8-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7daf8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7daf8-130">CommonParameters</span></span>
<span data-ttu-id="7daf8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7daf8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7daf8-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7daf8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7daf8-133">입력</span><span class="sxs-lookup"><span data-stu-id="7daf8-133">INPUTS</span></span>

## <span data-ttu-id="7daf8-134">출력</span><span class="sxs-lookup"><span data-stu-id="7daf8-134">OUTPUTS</span></span>

## <span data-ttu-id="7daf8-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7daf8-135">NOTES</span></span>

## <span data-ttu-id="7daf8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7daf8-136">RELATED LINKS</span></span>

[<span data-ttu-id="7daf8-137">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7daf8-137">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7daf8-138">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7daf8-138">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7daf8-139">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7daf8-139">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


