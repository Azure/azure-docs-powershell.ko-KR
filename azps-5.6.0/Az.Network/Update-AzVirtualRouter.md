---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: 119dec74416b8447d04aef7ae101016490408b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951568"
---
# <span data-ttu-id="6b89c-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6b89c-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="6b89c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b89c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b89c-103">가상 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="6b89c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b89c-104">SYNTAX</span></span>

### <span data-ttu-id="6b89c-105">VirtualRouterNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6b89c-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b89c-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b89c-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b89c-107">설명</span><span class="sxs-lookup"><span data-stu-id="6b89c-107">DESCRIPTION</span></span>
<span data-ttu-id="6b89c-108">분기 트래픽에 분기를 사용하도록 설정하거나 사용하지 않도록 가상 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="6b89c-109">예제</span><span class="sxs-lookup"><span data-stu-id="6b89c-109">EXAMPLES</span></span>

### <span data-ttu-id="6b89c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b89c-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="6b89c-111">분기 트래픽에 분기를 허용하도록 Virtual 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="6b89c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6b89c-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="6b89c-113">분기 트래픽을 차단하기 위해 Virtual 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="6b89c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b89c-114">PARAMETERS</span></span>

### <span data-ttu-id="6b89c-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="6b89c-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="6b89c-116">가상 라우터에 대한 분기 트래픽을 분기할 수 있도록 플래그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-116">Flag to allow branch to branch traffic for virtual router.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b89c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b89c-117">-DefaultProfile</span></span>
<span data-ttu-id="6b89c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b89c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b89c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b89c-120">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b89c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b89c-121">-ResourceId</span></span>
<span data-ttu-id="6b89c-122">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="6b89c-123">-라우터 이름</span><span class="sxs-lookup"><span data-stu-id="6b89c-123">-RouterName</span></span>
<span data-ttu-id="6b89c-124">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b89c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b89c-125">CommonParameters</span></span>
<span data-ttu-id="6b89c-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b89c-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b89c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b89c-128">입력</span><span class="sxs-lookup"><span data-stu-id="6b89c-128">INPUTS</span></span>

### <span data-ttu-id="6b89c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6b89c-129">System.String</span></span>

## <span data-ttu-id="6b89c-130">출력</span><span class="sxs-lookup"><span data-stu-id="6b89c-130">OUTPUTS</span></span>

### <span data-ttu-id="6b89c-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6b89c-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="6b89c-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b89c-132">NOTES</span></span>

## <span data-ttu-id="6b89c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b89c-133">RELATED LINKS</span></span>
