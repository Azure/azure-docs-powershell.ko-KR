---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: e3b3b0a0990f8c72fcd18d8828ae97d5c1a8a5aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015040"
---
# <span data-ttu-id="b34a9-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b34a9-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="b34a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b34a9-103">Azure ExpressRoutePortIdentity를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="b34a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="b34a9-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="b34a9-105">DESCRIPTION</span></span>
<span data-ttu-id="b34a9-106">**New-AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort IDENTITY 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="b34a9-107">**New-AzExpressRoutePort** 또는 **Set-AzExpressRoutePort를** 사용하여 Azure ExpressRoutePort에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="b34a9-108">예제</span><span class="sxs-lookup"><span data-stu-id="b34a9-108">EXAMPLES</span></span>

### <span data-ttu-id="b34a9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b34a9-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="b34a9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b34a9-110">PARAMETERS</span></span>

### <span data-ttu-id="b34a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34a9-111">-DefaultProfile</span></span>
<span data-ttu-id="b34a9-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34a9-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="b34a9-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="b34a9-114">ExpressRoutePort에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="b34a9-115">-확인</span><span class="sxs-lookup"><span data-stu-id="b34a9-115">-Confirm</span></span>
<span data-ttu-id="b34a9-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34a9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34a9-117">-WhatIf</span></span>
<span data-ttu-id="b34a9-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34a9-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34a9-120">CommonParameters</span></span>
<span data-ttu-id="b34a9-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b34a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34a9-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b34a9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34a9-123">입력</span><span class="sxs-lookup"><span data-stu-id="b34a9-123">INPUTS</span></span>

### <span data-ttu-id="b34a9-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b34a9-124">System.String</span></span>

## <span data-ttu-id="b34a9-125">출력</span><span class="sxs-lookup"><span data-stu-id="b34a9-125">OUTPUTS</span></span>

### <span data-ttu-id="b34a9-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b34a9-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="b34a9-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b34a9-127">NOTES</span></span>

## <span data-ttu-id="b34a9-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b34a9-128">RELATED LINKS</span></span>
[<span data-ttu-id="b34a9-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b34a9-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b34a9-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b34a9-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b34a9-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b34a9-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)