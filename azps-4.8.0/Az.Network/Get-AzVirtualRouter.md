---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214130"
---
# <span data-ttu-id="cf41a-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cf41a-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="cf41a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf41a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf41a-103">Azure VirtualRouter 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf41a-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="cf41a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf41a-104">SYNTAX</span></span>

### <span data-ttu-id="cf41a-105">VirtualRouterSubscriptionIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf41a-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf41a-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf41a-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf41a-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf41a-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf41a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cf41a-108">DESCRIPTION</span></span>
<span data-ttu-id="cf41a-109">**AzVirtualRouter** Cmdlet은 Azure virtualrouter를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf41a-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="cf41a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cf41a-110">EXAMPLES</span></span>

### <span data-ttu-id="cf41a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf41a-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="cf41a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="cf41a-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="cf41a-113">변수</span><span class="sxs-lookup"><span data-stu-id="cf41a-113">PARAMETERS</span></span>

### <span data-ttu-id="cf41a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf41a-114">-DefaultProfile</span></span>
<span data-ttu-id="cf41a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf41a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf41a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf41a-116">-ResourceGroupName</span></span>
<span data-ttu-id="cf41a-117">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf41a-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="cf41a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf41a-118">-ResourceId</span></span>
<span data-ttu-id="cf41a-119">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="cf41a-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="cf41a-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="cf41a-120">-RouterName</span></span>
<span data-ttu-id="cf41a-121">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf41a-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="cf41a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf41a-122">CommonParameters</span></span>
<span data-ttu-id="cf41a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf41a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf41a-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf41a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf41a-125">입력</span><span class="sxs-lookup"><span data-stu-id="cf41a-125">INPUTS</span></span>

### <span data-ttu-id="cf41a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf41a-126">System.String</span></span>

## <span data-ttu-id="cf41a-127">출력</span><span class="sxs-lookup"><span data-stu-id="cf41a-127">OUTPUTS</span></span>

### <span data-ttu-id="cf41a-128">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cf41a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="cf41a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="cf41a-129">NOTES</span></span>

## <span data-ttu-id="cf41a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf41a-130">RELATED LINKS</span></span>
