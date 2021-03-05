---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: e03ec2b7f2ceba70ba3037bbcad232dbfa7490de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976539"
---
# <span data-ttu-id="58747-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="58747-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="58747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58747-102">SYNOPSIS</span></span>
<span data-ttu-id="58747-103">수정된 IPAllocation을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="58747-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="58747-104">구문</span><span class="sxs-lookup"><span data-stu-id="58747-104">SYNTAX</span></span>

### <span data-ttu-id="58747-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="58747-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58747-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58747-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58747-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58747-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58747-108">설명</span><span class="sxs-lookup"><span data-stu-id="58747-108">DESCRIPTION</span></span>
<span data-ttu-id="58747-109">**Set-AzIpAllocation** cmdlet은 Azure IpAllocation을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="58747-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="58747-110">예제</span><span class="sxs-lookup"><span data-stu-id="58747-110">EXAMPLES</span></span>

### <span data-ttu-id="58747-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="58747-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="58747-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="58747-112">PARAMETERS</span></span>

### <span data-ttu-id="58747-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58747-113">-AsJob</span></span>
<span data-ttu-id="58747-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="58747-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58747-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58747-115">-DefaultProfile</span></span>
<span data-ttu-id="58747-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58747-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58747-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58747-117">-InputObject</span></span>
<span data-ttu-id="58747-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="58747-118">The IpAllocation</span></span>

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

### <span data-ttu-id="58747-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="58747-119">-IpAllocationTag</span></span>
<span data-ttu-id="58747-120">IP 할당의 할당 태그</span><span class="sxs-lookup"><span data-stu-id="58747-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="58747-121">-Name</span><span class="sxs-lookup"><span data-stu-id="58747-121">-Name</span></span>
<span data-ttu-id="58747-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58747-122">The resource name.</span></span>

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

### <span data-ttu-id="58747-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58747-123">-ResourceGroupName</span></span>
<span data-ttu-id="58747-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58747-124">The resource group name.</span></span>

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

### <span data-ttu-id="58747-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58747-125">-ResourceId</span></span>
<span data-ttu-id="58747-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="58747-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="58747-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="58747-127">-Tag</span></span>
<span data-ttu-id="58747-128">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="58747-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="58747-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58747-129">CommonParameters</span></span>
<span data-ttu-id="58747-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58747-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58747-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58747-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58747-132">입력</span><span class="sxs-lookup"><span data-stu-id="58747-132">INPUTS</span></span>

### <span data-ttu-id="58747-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="58747-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="58747-134">출력</span><span class="sxs-lookup"><span data-stu-id="58747-134">OUTPUTS</span></span>

### <span data-ttu-id="58747-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="58747-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="58747-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58747-136">NOTES</span></span>

## <span data-ttu-id="58747-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58747-137">RELATED LINKS</span></span>
