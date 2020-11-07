---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: ad8795016fc10212a885267d23a61ddc7224c906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871133"
---
# <span data-ttu-id="8a19f-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a19f-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="8a19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a19f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a19f-103">Application gateway의 자동 크기 조정 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="8a19f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a19f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a19f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a19f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a19f-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet은 응용 프로그램 게이트웨이의 기존 자동 크기 조정 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="8a19f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a19f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a19f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a19f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="8a19f-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="8a19f-110">두 번째 명령은 응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="8a19f-111">세 번째 명령은 Azure의 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="8a19f-112">변수</span><span class="sxs-lookup"><span data-stu-id="8a19f-112">PARAMETERS</span></span>

### <span data-ttu-id="8a19f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a19f-113">-ApplicationGateway</span></span>
<span data-ttu-id="8a19f-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a19f-114">The applicationGateway</span></span>

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

### <span data-ttu-id="8a19f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a19f-115">-DefaultProfile</span></span>
<span data-ttu-id="8a19f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a19f-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="8a19f-117">-MaxCapacity</span></span>
<span data-ttu-id="8a19f-118">응용 프로그램 게이트웨이의 최대 용량.</span><span class="sxs-lookup"><span data-stu-id="8a19f-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a19f-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="8a19f-119">-MinCapacity</span></span>
<span data-ttu-id="8a19f-120">Application gateway의 최소 용량.</span><span class="sxs-lookup"><span data-stu-id="8a19f-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a19f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8a19f-121">-Confirm</span></span>
<span data-ttu-id="8a19f-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a19f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a19f-123">-WhatIf</span></span>
<span data-ttu-id="8a19f-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a19f-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a19f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a19f-126">CommonParameters</span></span>
<span data-ttu-id="8a19f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a19f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a19f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a19f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a19f-129">입력</span><span class="sxs-lookup"><span data-stu-id="8a19f-129">INPUTS</span></span>

### <span data-ttu-id="8a19f-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a19f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a19f-131">출력</span><span class="sxs-lookup"><span data-stu-id="8a19f-131">OUTPUTS</span></span>

### <span data-ttu-id="8a19f-132">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a19f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a19f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8a19f-133">NOTES</span></span>

## <span data-ttu-id="8a19f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a19f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8a19f-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a19f-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="8a19f-136">새로운 AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a19f-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="8a19f-137">제거-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a19f-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
