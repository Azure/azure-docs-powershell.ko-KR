---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213025"
---
# <span data-ttu-id="5ae9f-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="5ae9f-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="5ae9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ae9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae9f-103">응용 프로그램 게이트웨이에 대 한 id 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="5ae9f-104">이는 사용자가 할당 한 id에 대 한 참조를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="5ae9f-105">구문과</span><span class="sxs-lookup"><span data-stu-id="5ae9f-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ae9f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="5ae9f-106">DESCRIPTION</span></span>
<span data-ttu-id="5ae9f-107">**AzApplicationGatewayIdentity** cmdlet은 응용 프로그램 게이트웨이 id 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="5ae9f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5ae9f-108">EXAMPLES</span></span>

### <span data-ttu-id="5ae9f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ae9f-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="5ae9f-110">이 예제에서는 사용자 지정 id를 만든 다음 Application Gateway와 함께 사용 되는 id 개체에서이를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="5ae9f-111">변수</span><span class="sxs-lookup"><span data-stu-id="5ae9f-111">PARAMETERS</span></span>

### <span data-ttu-id="5ae9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae9f-112">-DefaultProfile</span></span>
<span data-ttu-id="5ae9f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ae9f-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="5ae9f-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="5ae9f-115">응용 프로그램 게이트웨이에 할당할 사용자 지정 id의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="5ae9f-116">-확인</span><span class="sxs-lookup"><span data-stu-id="5ae9f-116">-Confirm</span></span>
<span data-ttu-id="5ae9f-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ae9f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ae9f-118">-WhatIf</span></span>
<span data-ttu-id="5ae9f-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ae9f-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ae9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae9f-121">CommonParameters</span></span>
<span data-ttu-id="5ae9f-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae9f-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae9f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae9f-124">입력</span><span class="sxs-lookup"><span data-stu-id="5ae9f-124">INPUTS</span></span>

### <span data-ttu-id="5ae9f-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ae9f-125">System.String</span></span>

## <span data-ttu-id="5ae9f-126">출력</span><span class="sxs-lookup"><span data-stu-id="5ae9f-126">OUTPUTS</span></span>

### <span data-ttu-id="5ae9f-127">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5ae9f-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="5ae9f-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5ae9f-128">NOTES</span></span>

## <span data-ttu-id="5ae9f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ae9f-129">RELATED LINKS</span></span>
