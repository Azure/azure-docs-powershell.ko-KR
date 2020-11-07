---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 0d99ec672d75844eca37cb63d63a2c6d7433d04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870565"
---
# <span data-ttu-id="4a994-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a994-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="4a994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a994-102">SYNOPSIS</span></span>
<span data-ttu-id="4a994-103">Application Gateway에 대 한 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="4a994-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a994-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a994-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4a994-105">DESCRIPTION</span></span>
<span data-ttu-id="4a994-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet은 Azure application gateway에 대 한 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="4a994-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4a994-107">EXAMPLES</span></span>

### <span data-ttu-id="4a994-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a994-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="4a994-109">첫 번째 명령은 최소 용량 3으로 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="4a994-110">두 번째 명령은 자동 크기 조정 구성을 사용 하 여 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="4a994-111">변수</span><span class="sxs-lookup"><span data-stu-id="4a994-111">PARAMETERS</span></span>

### <span data-ttu-id="4a994-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a994-112">-DefaultProfile</span></span>
<span data-ttu-id="4a994-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a994-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="4a994-114">-MaxCapacity</span></span>
<span data-ttu-id="4a994-115">항상 application gateway에 대해 사용할 수 있는 최대 용량 단위 이며, 요금이 부과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="4a994-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="4a994-116">-MinCapacity</span></span>
<span data-ttu-id="4a994-117">항상 응용 프로그램 게이트웨이에 대해 사용할 수 있는 최소 용량 단위 이며, 충전 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="4a994-118">-확인</span><span class="sxs-lookup"><span data-stu-id="4a994-118">-Confirm</span></span>
<span data-ttu-id="4a994-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a994-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a994-120">-WhatIf</span></span>
<span data-ttu-id="4a994-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a994-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a994-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a994-123">CommonParameters</span></span>
<span data-ttu-id="4a994-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a994-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a994-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a994-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a994-126">입력</span><span class="sxs-lookup"><span data-stu-id="4a994-126">INPUTS</span></span>

### <span data-ttu-id="4a994-127">않아야</span><span class="sxs-lookup"><span data-stu-id="4a994-127">None</span></span>

## <span data-ttu-id="4a994-128">출력</span><span class="sxs-lookup"><span data-stu-id="4a994-128">OUTPUTS</span></span>

### <span data-ttu-id="4a994-129">PSApplicationGatewayAutoscaleConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4a994-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="4a994-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4a994-130">NOTES</span></span>

## <span data-ttu-id="4a994-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a994-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a994-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a994-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="4a994-133">제거-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a994-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="4a994-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a994-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
