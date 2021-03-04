---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 202801e39e62b265b39036793ed4369a5d98bf2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008715"
---
# <span data-ttu-id="0fd2e-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fd2e-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0fd2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fd2e-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd2e-103">애플리케이션 게이트웨이에서 백 엔드 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="0fd2e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0fd2e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd2e-105">설명</span><span class="sxs-lookup"><span data-stu-id="0fd2e-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd2e-106">**Remove-AzApplicationGatewayBackendAddressPool** cmdlet은 Azure 애플리케이션 게이트웨이에서 백 엔드 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="0fd2e-107">예제</span><span class="sxs-lookup"><span data-stu-id="0fd2e-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd2e-108">예제 1: 애플리케이션 게이트웨이에서 백 엔드 주소 풀 제거</span><span class="sxs-lookup"><span data-stu-id="0fd2e-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="0fd2e-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="0fd2e-110">두 번째 명령은 애플리케이션 게이트웨이에서 BackEndPool02라는 백 엔드 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="0fd2e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0fd2e-111">PARAMETERS</span></span>

### <span data-ttu-id="0fd2e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fd2e-112">-ApplicationGateway</span></span>
<span data-ttu-id="0fd2e-113">이 cmdlet이 백 엔드 주소 풀을 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd2e-114">-DefaultProfile</span></span>
<span data-ttu-id="0fd2e-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd2e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0fd2e-116">-Name</span></span>
<span data-ttu-id="0fd2e-117">이 cmdlet이 제거한 백 엔드 주소 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd2e-118">-확인</span><span class="sxs-lookup"><span data-stu-id="0fd2e-118">-Confirm</span></span>
<span data-ttu-id="0fd2e-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd2e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd2e-120">-WhatIf</span></span>
<span data-ttu-id="0fd2e-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd2e-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd2e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd2e-123">CommonParameters</span></span>
<span data-ttu-id="0fd2e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd2e-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd2e-126">입력</span><span class="sxs-lookup"><span data-stu-id="0fd2e-126">INPUTS</span></span>

### <span data-ttu-id="0fd2e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fd2e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fd2e-128">출력</span><span class="sxs-lookup"><span data-stu-id="0fd2e-128">OUTPUTS</span></span>

### <span data-ttu-id="0fd2e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fd2e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0fd2e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0fd2e-130">NOTES</span></span>

## <span data-ttu-id="0fd2e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fd2e-131">RELATED LINKS</span></span>

[<span data-ttu-id="0fd2e-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fd2e-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0fd2e-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fd2e-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0fd2e-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fd2e-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0fd2e-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fd2e-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


