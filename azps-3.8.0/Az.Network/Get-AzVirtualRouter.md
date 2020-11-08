---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034826"
---
# <span data-ttu-id="e1147-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1147-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="e1147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1147-102">SYNOPSIS</span></span>
<span data-ttu-id="e1147-103">Azure VirtualRouter 가져오기</span><span class="sxs-lookup"><span data-stu-id="e1147-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="e1147-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1147-104">SYNTAX</span></span>

### <span data-ttu-id="e1147-105">VirtualRouterNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1147-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1147-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1147-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1147-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e1147-107">DESCRIPTION</span></span>
<span data-ttu-id="e1147-108">**AzVirtualRouter** Cmdlet은 Azure virtualrouter를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1147-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="e1147-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e1147-109">EXAMPLES</span></span>

### <span data-ttu-id="e1147-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1147-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="e1147-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="e1147-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="e1147-112">변수</span><span class="sxs-lookup"><span data-stu-id="e1147-112">PARAMETERS</span></span>

### <span data-ttu-id="e1147-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1147-113">-DefaultProfile</span></span>
<span data-ttu-id="e1147-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1147-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1147-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1147-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1147-116">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1147-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1147-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1147-117">-ResourceId</span></span>
<span data-ttu-id="e1147-118">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="e1147-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1147-119">-RouterName</span><span class="sxs-lookup"><span data-stu-id="e1147-119">-RouterName</span></span>
<span data-ttu-id="e1147-120">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1147-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1147-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1147-121">CommonParameters</span></span>
<span data-ttu-id="e1147-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1147-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1147-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1147-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1147-124">입력</span><span class="sxs-lookup"><span data-stu-id="e1147-124">INPUTS</span></span>

### <span data-ttu-id="e1147-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1147-125">System.String</span></span>

## <span data-ttu-id="e1147-126">출력</span><span class="sxs-lookup"><span data-stu-id="e1147-126">OUTPUTS</span></span>

### <span data-ttu-id="e1147-127">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1147-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e1147-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e1147-128">NOTES</span></span>

## <span data-ttu-id="e1147-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1147-129">RELATED LINKS</span></span>
