---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056193"
---
# <span data-ttu-id="feee9-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="feee9-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="feee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feee9-102">SYNOPSIS</span></span>
<span data-ttu-id="feee9-103">Azure ExpressRoutePortIdentity를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="feee9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="feee9-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feee9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="feee9-105">DESCRIPTION</span></span>
<span data-ttu-id="feee9-106">**AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort Identity 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="feee9-107">**New-AzExpressRoutePort** 또는 **Set-AzExpressRoutePort** 를 사용 하 여 Azure ExpressRoutePort에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="feee9-108">예제의</span><span class="sxs-lookup"><span data-stu-id="feee9-108">EXAMPLES</span></span>

### <span data-ttu-id="feee9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="feee9-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="feee9-110">변수</span><span class="sxs-lookup"><span data-stu-id="feee9-110">PARAMETERS</span></span>

### <span data-ttu-id="feee9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feee9-111">-DefaultProfile</span></span>
<span data-ttu-id="feee9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feee9-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="feee9-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="feee9-114">ExpressRoutePort에 할당할 사용자 지정 id의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="feee9-115">-확인</span><span class="sxs-lookup"><span data-stu-id="feee9-115">-Confirm</span></span>
<span data-ttu-id="feee9-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feee9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feee9-117">-WhatIf</span></span>
<span data-ttu-id="feee9-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feee9-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feee9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feee9-120">CommonParameters</span></span>
<span data-ttu-id="feee9-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="feee9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feee9-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feee9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feee9-123">입력</span><span class="sxs-lookup"><span data-stu-id="feee9-123">INPUTS</span></span>

### <span data-ttu-id="feee9-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="feee9-124">System.String</span></span>

## <span data-ttu-id="feee9-125">출력</span><span class="sxs-lookup"><span data-stu-id="feee9-125">OUTPUTS</span></span>

### <span data-ttu-id="feee9-126">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="feee9-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="feee9-127">상속자</span><span class="sxs-lookup"><span data-stu-id="feee9-127">NOTES</span></span>

## <span data-ttu-id="feee9-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feee9-128">RELATED LINKS</span></span>
[<span data-ttu-id="feee9-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="feee9-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="feee9-130">제거-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="feee9-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="feee9-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="feee9-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)