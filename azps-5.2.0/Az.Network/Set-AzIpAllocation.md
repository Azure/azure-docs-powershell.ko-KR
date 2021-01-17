---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339914"
---
# <span data-ttu-id="92026-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="92026-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="92026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92026-102">SYNOPSIS</span></span>
<span data-ttu-id="92026-103">수정된 IpAllocation을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="92026-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="92026-104">구문</span><span class="sxs-lookup"><span data-stu-id="92026-104">SYNTAX</span></span>

### <span data-ttu-id="92026-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92026-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92026-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92026-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92026-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92026-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92026-108">설명</span><span class="sxs-lookup"><span data-stu-id="92026-108">DESCRIPTION</span></span>
<span data-ttu-id="92026-109">**Set-AzIpAllocation** cmdlet은 Azure IpAllocation을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="92026-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="92026-110">예제</span><span class="sxs-lookup"><span data-stu-id="92026-110">EXAMPLES</span></span>

### <span data-ttu-id="92026-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="92026-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="92026-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92026-112">PARAMETERS</span></span>

### <span data-ttu-id="92026-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92026-113">-AsJob</span></span>
<span data-ttu-id="92026-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="92026-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92026-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92026-115">-DefaultProfile</span></span>
<span data-ttu-id="92026-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92026-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92026-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92026-117">-InputObject</span></span>
<span data-ttu-id="92026-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="92026-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="92026-119">-IpAllocationTag</span></span>
<span data-ttu-id="92026-120">IP 할당의 할당 태그</span><span class="sxs-lookup"><span data-stu-id="92026-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92026-121">-Name</span></span>
<span data-ttu-id="92026-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92026-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92026-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92026-123">-ResourceGroupName</span></span>
<span data-ttu-id="92026-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92026-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92026-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92026-125">-ResourceId</span></span>
<span data-ttu-id="92026-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="92026-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="92026-127">-Tag</span></span>
<span data-ttu-id="92026-128">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="92026-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92026-129">CommonParameters</span></span>
<span data-ttu-id="92026-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92026-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92026-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92026-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92026-132">입력</span><span class="sxs-lookup"><span data-stu-id="92026-132">INPUTS</span></span>

### <span data-ttu-id="92026-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="92026-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="92026-134">출력</span><span class="sxs-lookup"><span data-stu-id="92026-134">OUTPUTS</span></span>

### <span data-ttu-id="92026-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="92026-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="92026-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92026-136">NOTES</span></span>

## <span data-ttu-id="92026-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92026-137">RELATED LINKS</span></span>
