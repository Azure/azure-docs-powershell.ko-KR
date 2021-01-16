---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351854"
---
# <span data-ttu-id="b7aa3-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="b7aa3-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="b7aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aa3-103">애플리케이션 게이트웨이에 대한 ID 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="b7aa3-104">사용자 할당 ID에 대한 참조를 보유합니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="b7aa3-105">구문</span><span class="sxs-lookup"><span data-stu-id="b7aa3-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7aa3-106">설명</span><span class="sxs-lookup"><span data-stu-id="b7aa3-106">DESCRIPTION</span></span>
<span data-ttu-id="b7aa3-107">**New-AzApplicationGatewayIdentity** cmdlet은 애플리케이션 게이트웨이 ID 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="b7aa3-108">예제</span><span class="sxs-lookup"><span data-stu-id="b7aa3-108">EXAMPLES</span></span>

### <span data-ttu-id="b7aa3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7aa3-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="b7aa3-110">이 예제에서는 사용자 할당 ID를 만든 다음 Application Gateway와 함께 사용되는 ID 개체에서 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="b7aa3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7aa3-111">PARAMETERS</span></span>

### <span data-ttu-id="b7aa3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aa3-112">-DefaultProfile</span></span>
<span data-ttu-id="b7aa3-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7aa3-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="b7aa3-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="b7aa3-115">Application Gateway에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="b7aa3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7aa3-116">-Confirm</span></span>
<span data-ttu-id="b7aa3-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7aa3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7aa3-118">-WhatIf</span></span>
<span data-ttu-id="b7aa3-119">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b7aa3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7aa3-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7aa3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aa3-121">CommonParameters</span></span>
<span data-ttu-id="b7aa3-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aa3-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7aa3-124">입력</span><span class="sxs-lookup"><span data-stu-id="b7aa3-124">INPUTS</span></span>

### <span data-ttu-id="b7aa3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b7aa3-125">System.String</span></span>

## <span data-ttu-id="b7aa3-126">출력</span><span class="sxs-lookup"><span data-stu-id="b7aa3-126">OUTPUTS</span></span>

### <span data-ttu-id="b7aa3-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b7aa3-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="b7aa3-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7aa3-128">NOTES</span></span>

## <span data-ttu-id="b7aa3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7aa3-129">RELATED LINKS</span></span>
