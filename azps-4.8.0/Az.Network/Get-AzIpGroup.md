---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214138"
---
# <span data-ttu-id="f965e-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f965e-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="f965e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f965e-102">SYNOPSIS</span></span>
<span data-ttu-id="f965e-103">Azure IpGroup 가져오기</span><span class="sxs-lookup"><span data-stu-id="f965e-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="f965e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f965e-104">SYNTAX</span></span>

### <span data-ttu-id="f965e-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f965e-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f965e-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f965e-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f965e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f965e-107">DESCRIPTION</span></span>
<span data-ttu-id="f965e-108">**AzIpGroup** Cmdlet은 Azure ipgroup을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f965e-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="f965e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f965e-109">EXAMPLES</span></span>

### <span data-ttu-id="f965e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f965e-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="f965e-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="f965e-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="f965e-112">변수</span><span class="sxs-lookup"><span data-stu-id="f965e-112">PARAMETERS</span></span>

### <span data-ttu-id="f965e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f965e-113">-DefaultProfile</span></span>
<span data-ttu-id="f965e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f965e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f965e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f965e-115">-Name</span></span>
<span data-ttu-id="f965e-116">Ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f965e-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="f965e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f965e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f965e-118">Ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f965e-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="f965e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f965e-119">-ResourceId</span></span>
<span data-ttu-id="f965e-120">Ipgroup의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f965e-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="f965e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f965e-121">CommonParameters</span></span>
<span data-ttu-id="f965e-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f965e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f965e-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f965e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f965e-124">입력</span><span class="sxs-lookup"><span data-stu-id="f965e-124">INPUTS</span></span>

### <span data-ttu-id="f965e-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f965e-125">System.String</span></span>

## <span data-ttu-id="f965e-126">출력</span><span class="sxs-lookup"><span data-stu-id="f965e-126">OUTPUTS</span></span>

### <span data-ttu-id="f965e-127">PSIpGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f965e-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="f965e-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f965e-128">NOTES</span></span>

## <span data-ttu-id="f965e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f965e-129">RELATED LINKS</span></span>
