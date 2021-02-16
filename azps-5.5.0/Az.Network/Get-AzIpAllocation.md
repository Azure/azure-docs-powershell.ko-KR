---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189772"
---
# <span data-ttu-id="8b618-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="8b618-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="8b618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b618-102">SYNOPSIS</span></span>
<span data-ttu-id="8b618-103">Azure IpAllocation을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b618-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="8b618-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b618-104">SYNTAX</span></span>

### <span data-ttu-id="8b618-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b618-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b618-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b618-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b618-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b618-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b618-108">설명</span><span class="sxs-lookup"><span data-stu-id="8b618-108">DESCRIPTION</span></span>
<span data-ttu-id="8b618-109">**Get-AzIpAllocation** cmdlet은 Azure IpAllocation을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b618-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="8b618-110">예제</span><span class="sxs-lookup"><span data-stu-id="8b618-110">EXAMPLES</span></span>

### <span data-ttu-id="8b618-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b618-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="8b618-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b618-112">PARAMETERS</span></span>

### <span data-ttu-id="8b618-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b618-113">-DefaultProfile</span></span>
<span data-ttu-id="8b618-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b618-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b618-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b618-115">-Name</span></span>
<span data-ttu-id="8b618-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b618-116">The resource name.</span></span>

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

### <span data-ttu-id="8b618-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b618-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b618-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b618-118">The resource group name.</span></span>

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

### <span data-ttu-id="8b618-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b618-119">-ResourceId</span></span>
<span data-ttu-id="8b618-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="8b618-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="8b618-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b618-121">CommonParameters</span></span>
<span data-ttu-id="8b618-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b618-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b618-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b618-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b618-124">입력</span><span class="sxs-lookup"><span data-stu-id="8b618-124">INPUTS</span></span>

### <span data-ttu-id="8b618-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8b618-125">System.String</span></span>

## <span data-ttu-id="8b618-126">출력</span><span class="sxs-lookup"><span data-stu-id="8b618-126">OUTPUTS</span></span>

### <span data-ttu-id="8b618-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="8b618-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="8b618-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b618-128">NOTES</span></span>

## <span data-ttu-id="8b618-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b618-129">RELATED LINKS</span></span>
