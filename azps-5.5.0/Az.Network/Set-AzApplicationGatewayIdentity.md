---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186897"
---
# <span data-ttu-id="8c503-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="8c503-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="8c503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c503-102">SYNOPSIS</span></span>
<span data-ttu-id="8c503-103">애플리케이션 게이트웨이에 할당된 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="8c503-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c503-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c503-105">설명</span><span class="sxs-lookup"><span data-stu-id="8c503-105">DESCRIPTION</span></span>
<span data-ttu-id="8c503-106">**Set-AzApplicationGatewayIdentity** cmdlet은 애플리케이션 게이트웨이에 할당된 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="8c503-107">예제</span><span class="sxs-lookup"><span data-stu-id="8c503-107">EXAMPLES</span></span>

### <span data-ttu-id="8c503-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8c503-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="8c503-109">이 예제에서는 기존 애플리케이션 게이트웨이에 사용자 할당 ID를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="8c503-110">참고: 이 ID는 인증서/비밀을 참조할 키 자격 증명에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="8c503-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c503-111">PARAMETERS</span></span>

### <span data-ttu-id="8c503-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c503-112">-ApplicationGateway</span></span>
<span data-ttu-id="8c503-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c503-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8c503-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c503-114">-DefaultProfile</span></span>
<span data-ttu-id="8c503-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c503-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="8c503-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="8c503-117">Application Gateway에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c503-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c503-118">-Confirm</span></span>
<span data-ttu-id="8c503-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c503-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c503-120">-WhatIf</span></span>
<span data-ttu-id="8c503-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8c503-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c503-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c503-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c503-123">CommonParameters</span></span>
<span data-ttu-id="8c503-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c503-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c503-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c503-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c503-126">입력</span><span class="sxs-lookup"><span data-stu-id="8c503-126">INPUTS</span></span>

### <span data-ttu-id="8c503-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c503-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="8c503-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8c503-128">System.String</span></span>

## <span data-ttu-id="8c503-129">출력</span><span class="sxs-lookup"><span data-stu-id="8c503-129">OUTPUTS</span></span>

### <span data-ttu-id="8c503-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c503-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8c503-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c503-131">NOTES</span></span>

## <span data-ttu-id="8c503-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c503-132">RELATED LINKS</span></span>
