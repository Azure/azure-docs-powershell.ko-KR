---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034809"
---
# <span data-ttu-id="a0274-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a0274-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a0274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0274-102">SYNOPSIS</span></span>
<span data-ttu-id="a0274-103">응용 프로그램 게이트웨이에 할당 된 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a0274-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0274-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0274-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0274-105">DESCRIPTION</span></span>
<span data-ttu-id="a0274-106">**AzApplicationGatewayIdentity** cmdlet은 응용 프로그램 게이트웨이에 할당 된 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="a0274-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a0274-107">EXAMPLES</span></span>

### <span data-ttu-id="a0274-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0274-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a0274-109">이 예제에서는 사용자가 할당 한 id를 기존 응용 프로그램 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="a0274-110">참고:이 id는 인증서/비밀을 참조 하는 keyvault에 대 한 액세스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="a0274-111">변수</span><span class="sxs-lookup"><span data-stu-id="a0274-111">PARAMETERS</span></span>

### <span data-ttu-id="a0274-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0274-112">-ApplicationGateway</span></span>
<span data-ttu-id="a0274-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0274-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a0274-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0274-114">-DefaultProfile</span></span>
<span data-ttu-id="a0274-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0274-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a0274-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a0274-117">응용 프로그램 게이트웨이에 할당할 사용자 지정 id의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="a0274-118">-확인</span><span class="sxs-lookup"><span data-stu-id="a0274-118">-Confirm</span></span>
<span data-ttu-id="a0274-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0274-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0274-120">-WhatIf</span></span>
<span data-ttu-id="a0274-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0274-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0274-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0274-123">CommonParameters</span></span>
<span data-ttu-id="a0274-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0274-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0274-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0274-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0274-126">입력</span><span class="sxs-lookup"><span data-stu-id="a0274-126">INPUTS</span></span>

### <span data-ttu-id="a0274-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0274-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="a0274-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0274-128">System.String</span></span>

## <span data-ttu-id="a0274-129">출력</span><span class="sxs-lookup"><span data-stu-id="a0274-129">OUTPUTS</span></span>

### <span data-ttu-id="a0274-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0274-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0274-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a0274-131">NOTES</span></span>

## <span data-ttu-id="a0274-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0274-132">RELATED LINKS</span></span>
