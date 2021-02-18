---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193273"
---
# <span data-ttu-id="7233e-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7233e-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="7233e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7233e-102">SYNOPSIS</span></span>
<span data-ttu-id="7233e-103">가상 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="7233e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7233e-104">SYNTAX</span></span>

### <span data-ttu-id="7233e-105">VirtualRouterNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7233e-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7233e-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7233e-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7233e-107">설명</span><span class="sxs-lookup"><span data-stu-id="7233e-107">DESCRIPTION</span></span>
<span data-ttu-id="7233e-108">분기-분기 트래픽을 활성화하거나 사용하지 않도록 가상 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="7233e-109">예제</span><span class="sxs-lookup"><span data-stu-id="7233e-109">EXAMPLES</span></span>

### <span data-ttu-id="7233e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7233e-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="7233e-111">분기-분기 트래픽을 허용하도록 가상 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="7233e-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7233e-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="7233e-113">분기-분기 트래픽을 차단하는 가상 라우터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="7233e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7233e-114">PARAMETERS</span></span>

### <span data-ttu-id="7233e-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="7233e-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="7233e-116">가상 라우터에 대한 분기-분기 트래픽을 허용하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="7233e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7233e-117">-DefaultProfile</span></span>
<span data-ttu-id="7233e-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7233e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7233e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7233e-120">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="7233e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7233e-121">-ResourceId</span></span>
<span data-ttu-id="7233e-122">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="7233e-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="7233e-123">-RouterName</span></span>
<span data-ttu-id="7233e-124">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="7233e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7233e-125">CommonParameters</span></span>
<span data-ttu-id="7233e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7233e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7233e-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7233e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7233e-128">입력</span><span class="sxs-lookup"><span data-stu-id="7233e-128">INPUTS</span></span>

### <span data-ttu-id="7233e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7233e-129">System.String</span></span>

## <span data-ttu-id="7233e-130">출력</span><span class="sxs-lookup"><span data-stu-id="7233e-130">OUTPUTS</span></span>

### <span data-ttu-id="7233e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7233e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="7233e-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7233e-132">NOTES</span></span>

## <span data-ttu-id="7233e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7233e-133">RELATED LINKS</span></span>
