---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216084"
---
# <span data-ttu-id="ba601-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ba601-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="ba601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba601-102">SYNOPSIS</span></span>
<span data-ttu-id="ba601-103">Azure IpGroup을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="ba601-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba601-104">SYNTAX</span></span>

### <span data-ttu-id="ba601-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba601-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba601-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba601-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba601-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba601-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba601-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ba601-108">DESCRIPTION</span></span>
<span data-ttu-id="ba601-109">AzIpGroup cmdlet이 Azure IpGroup을 삭제 **함**</span><span class="sxs-lookup"><span data-stu-id="ba601-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="ba601-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ba601-110">EXAMPLES</span></span>

### <span data-ttu-id="ba601-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba601-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="ba601-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ba601-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="ba601-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="ba601-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="ba601-114">변수</span><span class="sxs-lookup"><span data-stu-id="ba601-114">PARAMETERS</span></span>

### <span data-ttu-id="ba601-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba601-115">-AsJob</span></span>
<span data-ttu-id="ba601-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ba601-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba601-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba601-117">-DefaultProfile</span></span>
<span data-ttu-id="ba601-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba601-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ba601-119">-Force</span></span>
<span data-ttu-id="ba601-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="ba601-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ba601-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="ba601-121">-IpGroup</span></span>
<span data-ttu-id="ba601-122">IpGroup 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba601-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ba601-123">-Name</span></span>
<span data-ttu-id="ba601-124">Ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba601-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba601-125">-PassThru</span></span>
<span data-ttu-id="ba601-126">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ba601-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba601-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba601-128">Ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="ba601-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba601-129">-ResourceId</span></span>
<span data-ttu-id="ba601-130">Ipgroup 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="ba601-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ba601-131">-Confirm</span></span>
<span data-ttu-id="ba601-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba601-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba601-133">-WhatIf</span></span>
<span data-ttu-id="ba601-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba601-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba601-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba601-136">CommonParameters</span></span>
<span data-ttu-id="ba601-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba601-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba601-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba601-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba601-139">입력</span><span class="sxs-lookup"><span data-stu-id="ba601-139">INPUTS</span></span>

### <span data-ttu-id="ba601-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba601-140">System.String</span></span>

### <span data-ttu-id="ba601-141">PSIpGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ba601-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="ba601-142">출력</span><span class="sxs-lookup"><span data-stu-id="ba601-142">OUTPUTS</span></span>

### <span data-ttu-id="ba601-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ba601-143">System.Boolean</span></span>

## <span data-ttu-id="ba601-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ba601-144">NOTES</span></span>

## <span data-ttu-id="ba601-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba601-145">RELATED LINKS</span></span>
