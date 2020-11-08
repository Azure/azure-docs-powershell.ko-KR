---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048855"
---
# <span data-ttu-id="7495c-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7495c-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="7495c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7495c-102">SYNOPSIS</span></span>
<span data-ttu-id="7495c-103">Application gateway에 대 한 PrivateLink 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="7495c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7495c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7495c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7495c-105">DESCRIPTION</span></span>
<span data-ttu-id="7495c-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet은 Azure application gateway에 대 한 privateLink 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="7495c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7495c-107">EXAMPLES</span></span>

### <span data-ttu-id="7495c-108">예제 1: PrivateLink 구성 설정</span><span class="sxs-lookup"><span data-stu-id="7495c-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="7495c-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7495c-110">두 번째 명령은 $privateLinkIpConfiguration 01에 저장 된 ip 구성을 사용 하도록 name privateLinkConfig01에 privateLink 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="7495c-111">변수</span><span class="sxs-lookup"><span data-stu-id="7495c-111">PARAMETERS</span></span>

### <span data-ttu-id="7495c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7495c-112">-ApplicationGateway</span></span>
<span data-ttu-id="7495c-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7495c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7495c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7495c-114">-DefaultProfile</span></span>
<span data-ttu-id="7495c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7495c-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7495c-116">-IpConfiguration</span></span>
<span data-ttu-id="7495c-117">IpConfiguration 목록</span><span class="sxs-lookup"><span data-stu-id="7495c-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="7495c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7495c-118">-Name</span></span>
<span data-ttu-id="7495c-119">PrivateLink 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="7495c-120">-확인</span><span class="sxs-lookup"><span data-stu-id="7495c-120">-Confirm</span></span>
<span data-ttu-id="7495c-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7495c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7495c-122">-WhatIf</span></span>
<span data-ttu-id="7495c-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7495c-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7495c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7495c-125">CommonParameters</span></span>
<span data-ttu-id="7495c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7495c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7495c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7495c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7495c-128">입력</span><span class="sxs-lookup"><span data-stu-id="7495c-128">INPUTS</span></span>

### <span data-ttu-id="7495c-129">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7495c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="7495c-130">PSApplicationGatewayPrivateLinkIpConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7495c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="7495c-131">출력</span><span class="sxs-lookup"><span data-stu-id="7495c-131">OUTPUTS</span></span>

### <span data-ttu-id="7495c-132">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7495c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7495c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7495c-133">NOTES</span></span>

## <span data-ttu-id="7495c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7495c-134">RELATED LINKS</span></span>

[<span data-ttu-id="7495c-135">새로운 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7495c-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7495c-136">추가-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7495c-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7495c-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7495c-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7495c-138">제거-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7495c-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)