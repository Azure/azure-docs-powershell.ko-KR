---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189764"
---
# <span data-ttu-id="31ab2-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="31ab2-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="31ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="31ab2-103">Azure IpGroup을 얻게</span><span class="sxs-lookup"><span data-stu-id="31ab2-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="31ab2-104">구문</span><span class="sxs-lookup"><span data-stu-id="31ab2-104">SYNTAX</span></span>

### <span data-ttu-id="31ab2-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ab2-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31ab2-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ab2-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ab2-107">설명</span><span class="sxs-lookup"><span data-stu-id="31ab2-107">DESCRIPTION</span></span>
<span data-ttu-id="31ab2-108">**Get-AzIpGroup** cmdlet은 Azure IpGroup을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31ab2-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="31ab2-109">예제</span><span class="sxs-lookup"><span data-stu-id="31ab2-109">EXAMPLES</span></span>

### <span data-ttu-id="31ab2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="31ab2-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="31ab2-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="31ab2-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="31ab2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31ab2-112">PARAMETERS</span></span>

### <span data-ttu-id="31ab2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ab2-113">-DefaultProfile</span></span>
<span data-ttu-id="31ab2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31ab2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ab2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="31ab2-115">-Name</span></span>
<span data-ttu-id="31ab2-116">ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31ab2-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="31ab2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ab2-117">-ResourceGroupName</span></span>
<span data-ttu-id="31ab2-118">ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31ab2-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="31ab2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31ab2-119">-ResourceId</span></span>
<span data-ttu-id="31ab2-120">ipgroup의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="31ab2-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="31ab2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ab2-121">CommonParameters</span></span>
<span data-ttu-id="31ab2-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31ab2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ab2-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31ab2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ab2-124">입력</span><span class="sxs-lookup"><span data-stu-id="31ab2-124">INPUTS</span></span>

### <span data-ttu-id="31ab2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="31ab2-125">System.String</span></span>

## <span data-ttu-id="31ab2-126">출력</span><span class="sxs-lookup"><span data-stu-id="31ab2-126">OUTPUTS</span></span>

### <span data-ttu-id="31ab2-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="31ab2-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="31ab2-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31ab2-128">NOTES</span></span>

## <span data-ttu-id="31ab2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31ab2-129">RELATED LINKS</span></span>
