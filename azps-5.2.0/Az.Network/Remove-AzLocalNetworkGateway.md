---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363497"
---
# <span data-ttu-id="88661-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="88661-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="88661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88661-102">SYNOPSIS</span></span>
<span data-ttu-id="88661-103">로컬 네트워크 게이트웨이를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="88661-104">구문</span><span class="sxs-lookup"><span data-stu-id="88661-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88661-105">설명</span><span class="sxs-lookup"><span data-stu-id="88661-105">DESCRIPTION</span></span>
<span data-ttu-id="88661-106">로컬 네트워크 게이트웨이는 VPN 디바이스 On-프레미스를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88661-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="88661-107">**Remove-AzLocalNetworkGateway** cmdlet은 이름 및 리소스 그룹 이름을 기준으로 프레미스 게이트웨이를 나타내는 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="88661-108">예제</span><span class="sxs-lookup"><span data-stu-id="88661-108">EXAMPLES</span></span>

### <span data-ttu-id="88661-109">예제 1: 로컬 네트워크 게이트웨이 삭제</span><span class="sxs-lookup"><span data-stu-id="88661-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="88661-110">리소스 그룹 "myRG" 내에서 "myLocalGW"라는 이름으로 로컬 네트워크 게이트웨이의 개체를 삭제합니다. 먼저 **Remove-AzVirtualNetworkGatewayConnection** cmdlet을 사용하여 로컬 네트워크 게이트웨이에 대한 모든 연결을 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="88661-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88661-111">PARAMETERS</span></span>

### <span data-ttu-id="88661-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88661-112">-AsJob</span></span>
<span data-ttu-id="88661-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="88661-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88661-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88661-114">-DefaultProfile</span></span>
<span data-ttu-id="88661-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88661-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88661-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88661-116">-Force</span></span>
<span data-ttu-id="88661-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88661-118">-Name</span><span class="sxs-lookup"><span data-stu-id="88661-118">-Name</span></span>
<span data-ttu-id="88661-119">이 cmdlet이 제거하는 로컬 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88661-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88661-120">-PassThru</span></span>
<span data-ttu-id="88661-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="88661-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88661-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88661-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88661-123">-ResourceGroupName</span></span>
<span data-ttu-id="88661-124">로컬 네트워크 게이트웨이를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="88661-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88661-125">-Confirm</span></span>
<span data-ttu-id="88661-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88661-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88661-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88661-127">-WhatIf</span></span>
<span data-ttu-id="88661-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="88661-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88661-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88661-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88661-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88661-130">CommonParameters</span></span>
<span data-ttu-id="88661-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88661-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88661-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88661-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88661-133">입력</span><span class="sxs-lookup"><span data-stu-id="88661-133">INPUTS</span></span>

### <span data-ttu-id="88661-134">System.String</span><span class="sxs-lookup"><span data-stu-id="88661-134">System.String</span></span>

## <span data-ttu-id="88661-135">출력</span><span class="sxs-lookup"><span data-stu-id="88661-135">OUTPUTS</span></span>

### <span data-ttu-id="88661-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88661-136">System.Boolean</span></span>

## <span data-ttu-id="88661-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88661-137">NOTES</span></span>

## <span data-ttu-id="88661-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88661-138">RELATED LINKS</span></span>

[<span data-ttu-id="88661-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="88661-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="88661-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="88661-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="88661-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="88661-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
