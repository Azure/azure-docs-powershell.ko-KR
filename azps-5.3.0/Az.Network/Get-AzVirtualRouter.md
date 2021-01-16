---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379814"
---
# <span data-ttu-id="91396-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="91396-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="91396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91396-102">SYNOPSIS</span></span>
<span data-ttu-id="91396-103">Azure VirtualRouter를 얻게</span><span class="sxs-lookup"><span data-stu-id="91396-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="91396-104">구문</span><span class="sxs-lookup"><span data-stu-id="91396-104">SYNTAX</span></span>

### <span data-ttu-id="91396-105">VirtualRouterSubscriptionIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="91396-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91396-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91396-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91396-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91396-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91396-108">설명</span><span class="sxs-lookup"><span data-stu-id="91396-108">DESCRIPTION</span></span>
<span data-ttu-id="91396-109">**Get-AzVirtualRouter** cmdlet은 Azure VirtualRouter를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="91396-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="91396-110">예제</span><span class="sxs-lookup"><span data-stu-id="91396-110">EXAMPLES</span></span>

### <span data-ttu-id="91396-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="91396-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="91396-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="91396-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="91396-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91396-113">PARAMETERS</span></span>

### <span data-ttu-id="91396-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91396-114">-DefaultProfile</span></span>
<span data-ttu-id="91396-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91396-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91396-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91396-116">-ResourceGroupName</span></span>
<span data-ttu-id="91396-117">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91396-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91396-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91396-118">-ResourceId</span></span>
<span data-ttu-id="91396-119">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="91396-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91396-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="91396-120">-RouterName</span></span>
<span data-ttu-id="91396-121">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91396-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91396-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91396-122">CommonParameters</span></span>
<span data-ttu-id="91396-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91396-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91396-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91396-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91396-125">입력</span><span class="sxs-lookup"><span data-stu-id="91396-125">INPUTS</span></span>

### <span data-ttu-id="91396-126">System.String</span><span class="sxs-lookup"><span data-stu-id="91396-126">System.String</span></span>

## <span data-ttu-id="91396-127">출력</span><span class="sxs-lookup"><span data-stu-id="91396-127">OUTPUTS</span></span>

### <span data-ttu-id="91396-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="91396-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="91396-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91396-129">NOTES</span></span>

## <span data-ttu-id="91396-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91396-130">RELATED LINKS</span></span>