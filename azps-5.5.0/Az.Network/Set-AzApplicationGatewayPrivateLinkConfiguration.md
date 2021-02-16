---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179380"
---
# <span data-ttu-id="5c0a0-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c0a0-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="5c0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0a0-103">애플리케이션 게이트웨이에 대한 PrivateLink 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="5c0a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c0a0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c0a0-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c0a0-105">DESCRIPTION</span></span>
<span data-ttu-id="5c0a0-106">**Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 privateLink 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="5c0a0-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c0a0-107">EXAMPLES</span></span>

### <span data-ttu-id="5c0a0-108">예제 1: PrivateLink 구성 설정</span><span class="sxs-lookup"><span data-stu-id="5c0a0-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="5c0a0-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c0a0-110">두 번째 명령은 privateLinkConfig01 이름으로 privateLink 구성을 설정하여 $privateLinkIpConfiguration 01에 저장된 ip 구성을 사용</span><span class="sxs-lookup"><span data-stu-id="5c0a0-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="5c0a0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c0a0-111">PARAMETERS</span></span>

### <span data-ttu-id="5c0a0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c0a0-112">-ApplicationGateway</span></span>
<span data-ttu-id="5c0a0-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c0a0-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0a0-114">-DefaultProfile</span></span>
<span data-ttu-id="5c0a0-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a0-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c0a0-116">-IpConfiguration</span></span>
<span data-ttu-id="5c0a0-117">ipConfiguration 목록</span><span class="sxs-lookup"><span data-stu-id="5c0a0-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5c0a0-118">-Name</span></span>
<span data-ttu-id="5c0a0-119">privateLink 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="5c0a0-119">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c0a0-120">-Confirm</span></span>
<span data-ttu-id="5c0a0-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0a0-122">-WhatIf</span></span>
<span data-ttu-id="5c0a0-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c0a0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0a0-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0a0-125">CommonParameters</span></span>
<span data-ttu-id="5c0a0-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0a0-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c0a0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0a0-128">입력</span><span class="sxs-lookup"><span data-stu-id="5c0a0-128">INPUTS</span></span>

### <span data-ttu-id="5c0a0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c0a0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="5c0a0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="5c0a0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="5c0a0-131">출력</span><span class="sxs-lookup"><span data-stu-id="5c0a0-131">OUTPUTS</span></span>

### <span data-ttu-id="5c0a0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c0a0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c0a0-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c0a0-133">NOTES</span></span>

## <span data-ttu-id="5c0a0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c0a0-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c0a0-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c0a0-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5c0a0-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c0a0-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5c0a0-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c0a0-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5c0a0-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c0a0-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)