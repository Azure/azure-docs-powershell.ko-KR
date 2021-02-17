---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206856"
---
# <span data-ttu-id="aad13-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad13-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="aad13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad13-102">SYNOPSIS</span></span>
<span data-ttu-id="aad13-103">Application Gateway에 대한 자동 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="aad13-104">구문</span><span class="sxs-lookup"><span data-stu-id="aad13-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad13-105">설명</span><span class="sxs-lookup"><span data-stu-id="aad13-105">DESCRIPTION</span></span>
<span data-ttu-id="aad13-106">**New-AzApplicationGatewayAutoscaleConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="aad13-107">예제</span><span class="sxs-lookup"><span data-stu-id="aad13-107">EXAMPLES</span></span>

### <span data-ttu-id="aad13-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aad13-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="aad13-109">첫 번째 명령은 최소 용량 3을 사용하여 자동 확장 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="aad13-110">두 번째 명령은 자동 조정 구성을 사용하여 애플리케이션 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="aad13-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad13-111">PARAMETERS</span></span>

### <span data-ttu-id="aad13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad13-112">-DefaultProfile</span></span>
<span data-ttu-id="aad13-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad13-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="aad13-114">-MaxCapacity</span></span>
<span data-ttu-id="aad13-115">애플리케이션 게이트웨이에 대해 항상 사용 가능 [및 청구]될 최대 용량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="aad13-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="aad13-116">-MinCapacity</span></span>
<span data-ttu-id="aad13-117">애플리케이션 게이트웨이에 대해 항상 사용 가능 [및 청구]될 최소 용량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="aad13-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aad13-118">-Confirm</span></span>
<span data-ttu-id="aad13-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aad13-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad13-120">-WhatIf</span></span>
<span data-ttu-id="aad13-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aad13-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad13-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aad13-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad13-123">CommonParameters</span></span>
<span data-ttu-id="aad13-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aad13-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad13-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aad13-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad13-126">입력</span><span class="sxs-lookup"><span data-stu-id="aad13-126">INPUTS</span></span>

### <span data-ttu-id="aad13-127">없음</span><span class="sxs-lookup"><span data-stu-id="aad13-127">None</span></span>

## <span data-ttu-id="aad13-128">출력</span><span class="sxs-lookup"><span data-stu-id="aad13-128">OUTPUTS</span></span>

### <span data-ttu-id="aad13-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad13-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="aad13-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aad13-130">NOTES</span></span>

## <span data-ttu-id="aad13-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aad13-131">RELATED LINKS</span></span>

[<span data-ttu-id="aad13-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad13-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="aad13-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad13-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="aad13-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad13-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
