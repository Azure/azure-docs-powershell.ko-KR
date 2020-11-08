---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: ad205aabc12a2f0d6abffd16b83dadfc9a34ff4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044022"
---
# <span data-ttu-id="03e65-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03e65-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="03e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e65-102">SYNOPSIS</span></span>
<span data-ttu-id="03e65-103">로컬 네트워크 게이트웨이를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="03e65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03e65-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e65-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03e65-105">DESCRIPTION</span></span>
<span data-ttu-id="03e65-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="03e65-107">**AzLocalNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 프레미스 게이트웨이를 나타내는 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="03e65-108">예제의</span><span class="sxs-lookup"><span data-stu-id="03e65-108">EXAMPLES</span></span>

### <span data-ttu-id="03e65-109">1: 로컬 네트워크 게이트웨이 삭제</span><span class="sxs-lookup"><span data-stu-id="03e65-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="03e65-110">리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 삭제 합니다. 참고: 먼저 **Remove-AzVirtualNetworkGatewayConnection** cmdlet을 사용 하 여 로컬 네트워크 게이트웨이에 대 한 모든 연결을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="03e65-111">변수</span><span class="sxs-lookup"><span data-stu-id="03e65-111">PARAMETERS</span></span>

### <span data-ttu-id="03e65-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03e65-112">-AsJob</span></span>
<span data-ttu-id="03e65-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03e65-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03e65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e65-114">-DefaultProfile</span></span>
<span data-ttu-id="03e65-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e65-116">-Force</span><span class="sxs-lookup"><span data-stu-id="03e65-116">-Force</span></span>
<span data-ttu-id="03e65-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03e65-118">-이름</span><span class="sxs-lookup"><span data-stu-id="03e65-118">-Name</span></span>
<span data-ttu-id="03e65-119">이 cmdlet이 제거 하는 로컬 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03e65-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03e65-120">-PassThru</span></span>
<span data-ttu-id="03e65-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03e65-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03e65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e65-123">-ResourceGroupName</span></span>
<span data-ttu-id="03e65-124">로컬 네트워크 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="03e65-125">-확인</span><span class="sxs-lookup"><span data-stu-id="03e65-125">-Confirm</span></span>
<span data-ttu-id="03e65-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e65-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e65-127">-WhatIf</span></span>
<span data-ttu-id="03e65-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e65-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e65-130">CommonParameters</span></span>
<span data-ttu-id="03e65-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e65-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e65-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e65-133">입력</span><span class="sxs-lookup"><span data-stu-id="03e65-133">INPUTS</span></span>

### <span data-ttu-id="03e65-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03e65-134">System.String</span></span>

## <span data-ttu-id="03e65-135">출력</span><span class="sxs-lookup"><span data-stu-id="03e65-135">OUTPUTS</span></span>

### <span data-ttu-id="03e65-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="03e65-136">System.Boolean</span></span>

## <span data-ttu-id="03e65-137">상속자</span><span class="sxs-lookup"><span data-stu-id="03e65-137">NOTES</span></span>

## <span data-ttu-id="03e65-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03e65-138">RELATED LINKS</span></span>

[<span data-ttu-id="03e65-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03e65-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="03e65-140">새로운 AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03e65-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="03e65-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03e65-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
