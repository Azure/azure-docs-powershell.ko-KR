---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 75a7afbb8997492e1b30ead7f745d2f5b6eb8b5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956896"
---
# <span data-ttu-id="d2e7a-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d2e7a-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="d2e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e7a-103">Azure IpGroup을 얻다</span><span class="sxs-lookup"><span data-stu-id="d2e7a-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="d2e7a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2e7a-104">SYNTAX</span></span>

### <span data-ttu-id="d2e7a-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2e7a-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2e7a-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2e7a-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e7a-107">설명</span><span class="sxs-lookup"><span data-stu-id="d2e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e7a-108">**Get-AzIpGroup** cmdlet은 Azure IpGroup을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e7a-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="d2e7a-109">예제</span><span class="sxs-lookup"><span data-stu-id="d2e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e7a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2e7a-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="d2e7a-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="d2e7a-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="d2e7a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d2e7a-112">PARAMETERS</span></span>

### <span data-ttu-id="d2e7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e7a-113">-DefaultProfile</span></span>
<span data-ttu-id="d2e7a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e7a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d2e7a-115">-Name</span></span>
<span data-ttu-id="d2e7a-116">ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e7a-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e7a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e7a-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2e7a-118">ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e7a-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e7a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e7a-119">-ResourceId</span></span>
<span data-ttu-id="d2e7a-120">ipgroup의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e7a-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e7a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e7a-121">CommonParameters</span></span>
<span data-ttu-id="d2e7a-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e7a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e7a-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2e7a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e7a-124">입력</span><span class="sxs-lookup"><span data-stu-id="d2e7a-124">INPUTS</span></span>

### <span data-ttu-id="d2e7a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d2e7a-125">System.String</span></span>

## <span data-ttu-id="d2e7a-126">출력</span><span class="sxs-lookup"><span data-stu-id="d2e7a-126">OUTPUTS</span></span>

### <span data-ttu-id="d2e7a-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d2e7a-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d2e7a-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2e7a-128">NOTES</span></span>

## <span data-ttu-id="d2e7a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2e7a-129">RELATED LINKS</span></span>
