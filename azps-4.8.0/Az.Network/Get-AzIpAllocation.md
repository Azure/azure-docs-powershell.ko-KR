---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214141"
---
# <span data-ttu-id="7d742-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="7d742-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="7d742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d742-102">SYNOPSIS</span></span>
<span data-ttu-id="7d742-103">Azure IpAllocation을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d742-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="7d742-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d742-104">SYNTAX</span></span>

### <span data-ttu-id="7d742-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d742-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d742-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d742-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d742-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d742-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d742-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7d742-108">DESCRIPTION</span></span>
<span data-ttu-id="7d742-109">**AzIpAllocation** Cmdlet은 Azure ip 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d742-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="7d742-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7d742-110">EXAMPLES</span></span>

### <span data-ttu-id="7d742-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d742-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="7d742-112">변수</span><span class="sxs-lookup"><span data-stu-id="7d742-112">PARAMETERS</span></span>

### <span data-ttu-id="7d742-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d742-113">-DefaultProfile</span></span>
<span data-ttu-id="7d742-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d742-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d742-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7d742-115">-Name</span></span>
<span data-ttu-id="7d742-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d742-116">The resource name.</span></span>

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

### <span data-ttu-id="7d742-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d742-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d742-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d742-118">The resource group name.</span></span>

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

### <span data-ttu-id="7d742-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d742-119">-ResourceId</span></span>
<span data-ttu-id="7d742-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="7d742-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="7d742-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d742-121">CommonParameters</span></span>
<span data-ttu-id="7d742-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d742-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d742-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d742-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d742-124">입력</span><span class="sxs-lookup"><span data-stu-id="7d742-124">INPUTS</span></span>

### <span data-ttu-id="7d742-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d742-125">System.String</span></span>

## <span data-ttu-id="7d742-126">출력</span><span class="sxs-lookup"><span data-stu-id="7d742-126">OUTPUTS</span></span>

### <span data-ttu-id="7d742-127">PSIpAllocation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7d742-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="7d742-128">상속자</span><span class="sxs-lookup"><span data-stu-id="7d742-128">NOTES</span></span>

## <span data-ttu-id="7d742-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d742-129">RELATED LINKS</span></span>
