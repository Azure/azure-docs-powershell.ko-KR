---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: f1cc98c8008d8f9eff47fa6f5172fb28a448c7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993804"
---
# <span data-ttu-id="e4d4f-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="e4d4f-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="e4d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d4f-103">애플리케이션 게이트웨이에 대한 ID 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="e4d4f-104">이렇게 하면 사용자 할당 ID에 대한 참조가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="e4d4f-105">구문</span><span class="sxs-lookup"><span data-stu-id="e4d4f-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d4f-106">설명</span><span class="sxs-lookup"><span data-stu-id="e4d4f-106">DESCRIPTION</span></span>
<span data-ttu-id="e4d4f-107">**New-AzApplicationGatewayIdentity** cmdlet은 애플리케이션 게이트웨이 ID 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="e4d4f-108">예제</span><span class="sxs-lookup"><span data-stu-id="e4d4f-108">EXAMPLES</span></span>

### <span data-ttu-id="e4d4f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4d4f-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="e4d4f-110">이 예제에서는 사용자 할당 ID를 만든 다음 Application Gateway와 함께 사용되는 ID 개체에서 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="e4d4f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4d4f-111">PARAMETERS</span></span>

### <span data-ttu-id="e4d4f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d4f-112">-DefaultProfile</span></span>
<span data-ttu-id="e4d4f-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d4f-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="e4d4f-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="e4d4f-115">Application Gateway에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="e4d4f-116">-확인</span><span class="sxs-lookup"><span data-stu-id="e4d4f-116">-Confirm</span></span>
<span data-ttu-id="e4d4f-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d4f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d4f-118">-WhatIf</span></span>
<span data-ttu-id="e4d4f-119">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d4f-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d4f-121">CommonParameters</span></span>
<span data-ttu-id="e4d4f-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d4f-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e4d4f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d4f-124">입력</span><span class="sxs-lookup"><span data-stu-id="e4d4f-124">INPUTS</span></span>

### <span data-ttu-id="e4d4f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e4d4f-125">System.String</span></span>

## <span data-ttu-id="e4d4f-126">출력</span><span class="sxs-lookup"><span data-stu-id="e4d4f-126">OUTPUTS</span></span>

### <span data-ttu-id="e4d4f-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e4d4f-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e4d4f-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4d4f-128">NOTES</span></span>

## <span data-ttu-id="e4d4f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4d4f-129">RELATED LINKS</span></span>
