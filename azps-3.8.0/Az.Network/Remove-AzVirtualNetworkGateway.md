---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: eec1fd885dd193ae69fd119a127634e2cfa19a51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043968"
---
# <span data-ttu-id="583db-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="583db-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="583db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="583db-102">SYNOPSIS</span></span>
<span data-ttu-id="583db-103">가상 네트워크 게이트웨이를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="583db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="583db-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="583db-105">DESCRIPTION</span></span>
<span data-ttu-id="583db-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="583db-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="583db-107">**AzVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="583db-108">예제의</span><span class="sxs-lookup"><span data-stu-id="583db-108">EXAMPLES</span></span>

### <span data-ttu-id="583db-109">1: 가상 네트워크 게이트웨이 삭제</span><span class="sxs-lookup"><span data-stu-id="583db-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="583db-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이의 개체를 삭제 합니다. 참고: 먼저 **AzVirtualNetworkGatewayConnection** cmdlet을 사용 하 여 가상 네트워크 게이트웨이에 대 한 모든 연결을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="583db-111">변수</span><span class="sxs-lookup"><span data-stu-id="583db-111">PARAMETERS</span></span>

### <span data-ttu-id="583db-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="583db-112">-AsJob</span></span>
<span data-ttu-id="583db-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="583db-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="583db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583db-114">-DefaultProfile</span></span>
<span data-ttu-id="583db-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="583db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583db-116">-Force</span><span class="sxs-lookup"><span data-stu-id="583db-116">-Force</span></span>
<span data-ttu-id="583db-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="583db-118">-이름</span><span class="sxs-lookup"><span data-stu-id="583db-118">-Name</span></span>
<span data-ttu-id="583db-119">이 cmdlet이 제거 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="583db-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="583db-120">-PassThru</span></span>
<span data-ttu-id="583db-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="583db-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="583db-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="583db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="583db-123">-ResourceGroupName</span></span>
<span data-ttu-id="583db-124">가상 네트워크 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="583db-125">-확인</span><span class="sxs-lookup"><span data-stu-id="583db-125">-Confirm</span></span>
<span data-ttu-id="583db-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583db-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583db-127">-WhatIf</span></span>
<span data-ttu-id="583db-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="583db-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="583db-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="583db-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583db-130">CommonParameters</span></span>
<span data-ttu-id="583db-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="583db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583db-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583db-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583db-133">입력</span><span class="sxs-lookup"><span data-stu-id="583db-133">INPUTS</span></span>

### <span data-ttu-id="583db-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="583db-134">System.String</span></span>

## <span data-ttu-id="583db-135">출력</span><span class="sxs-lookup"><span data-stu-id="583db-135">OUTPUTS</span></span>

### <span data-ttu-id="583db-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="583db-136">System.Boolean</span></span>

## <span data-ttu-id="583db-137">상속자</span><span class="sxs-lookup"><span data-stu-id="583db-137">NOTES</span></span>

## <span data-ttu-id="583db-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="583db-138">RELATED LINKS</span></span>

[<span data-ttu-id="583db-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="583db-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="583db-140">새로운 AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="583db-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="583db-141">다시 설정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="583db-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="583db-142">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="583db-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="583db-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="583db-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
