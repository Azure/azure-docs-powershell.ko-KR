---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041661"
---
# <span data-ttu-id="a06a2-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a06a2-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="a06a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a06a2-103">Azure ExpressRoutePortIdentity를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="a06a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a06a2-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a06a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a06a2-106">**AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort Identity 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="a06a2-107">**New-AzExpressRoutePort** 또는 **Set-AzExpressRoutePort** 를 사용 하 여 Azure ExpressRoutePort에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="a06a2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a06a2-108">EXAMPLES</span></span>

### <span data-ttu-id="a06a2-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a06a2-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="a06a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="a06a2-110">PARAMETERS</span></span>

### <span data-ttu-id="a06a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06a2-111">-DefaultProfile</span></span>
<span data-ttu-id="a06a2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06a2-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a06a2-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a06a2-114">ExpressRoutePort에 할당할 사용자 지정 id의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="a06a2-115">-확인</span><span class="sxs-lookup"><span data-stu-id="a06a2-115">-Confirm</span></span>
<span data-ttu-id="a06a2-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a06a2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06a2-117">-WhatIf</span></span>
<span data-ttu-id="a06a2-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a06a2-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a06a2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06a2-120">CommonParameters</span></span>
<span data-ttu-id="a06a2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06a2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06a2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06a2-123">입력</span><span class="sxs-lookup"><span data-stu-id="a06a2-123">INPUTS</span></span>

### <span data-ttu-id="a06a2-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a06a2-124">System.String</span></span>

## <span data-ttu-id="a06a2-125">출력</span><span class="sxs-lookup"><span data-stu-id="a06a2-125">OUTPUTS</span></span>

### <span data-ttu-id="a06a2-126">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a06a2-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="a06a2-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a06a2-127">NOTES</span></span>

## <span data-ttu-id="a06a2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a06a2-128">RELATED LINKS</span></span>
[<span data-ttu-id="a06a2-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a06a2-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="a06a2-130">제거-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a06a2-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="a06a2-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a06a2-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)