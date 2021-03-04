---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: c08a148d1c58e08daa2fce8cd1e195887a264f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956907"
---
# <span data-ttu-id="633cd-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="633cd-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="633cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="633cd-102">SYNOPSIS</span></span>
<span data-ttu-id="633cd-103">Azure IpAllocation을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="633cd-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="633cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="633cd-104">SYNTAX</span></span>

### <span data-ttu-id="633cd-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="633cd-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="633cd-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="633cd-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="633cd-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="633cd-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="633cd-108">설명</span><span class="sxs-lookup"><span data-stu-id="633cd-108">DESCRIPTION</span></span>
<span data-ttu-id="633cd-109">**Get-AzIpAllocation** cmdlet은 Azure IpAllocation을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="633cd-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="633cd-110">예제</span><span class="sxs-lookup"><span data-stu-id="633cd-110">EXAMPLES</span></span>

### <span data-ttu-id="633cd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="633cd-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="633cd-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="633cd-112">PARAMETERS</span></span>

### <span data-ttu-id="633cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633cd-113">-DefaultProfile</span></span>
<span data-ttu-id="633cd-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="633cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="633cd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="633cd-115">-Name</span></span>
<span data-ttu-id="633cd-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="633cd-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633cd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633cd-117">-ResourceGroupName</span></span>
<span data-ttu-id="633cd-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="633cd-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633cd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="633cd-119">-ResourceId</span></span>
<span data-ttu-id="633cd-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="633cd-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="633cd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633cd-121">CommonParameters</span></span>
<span data-ttu-id="633cd-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="633cd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633cd-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="633cd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633cd-124">입력</span><span class="sxs-lookup"><span data-stu-id="633cd-124">INPUTS</span></span>

### <span data-ttu-id="633cd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="633cd-125">System.String</span></span>

## <span data-ttu-id="633cd-126">출력</span><span class="sxs-lookup"><span data-stu-id="633cd-126">OUTPUTS</span></span>

### <span data-ttu-id="633cd-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="633cd-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="633cd-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="633cd-128">NOTES</span></span>

## <span data-ttu-id="633cd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="633cd-129">RELATED LINKS</span></span>
