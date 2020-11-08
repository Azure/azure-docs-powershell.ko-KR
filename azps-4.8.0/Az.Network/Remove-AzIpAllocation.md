---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056157"
---
# <span data-ttu-id="da751-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="da751-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="da751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da751-102">SYNOPSIS</span></span>
<span data-ttu-id="da751-103">Azure IpAllocation을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="da751-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="da751-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da751-104">SYNTAX</span></span>

### <span data-ttu-id="da751-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="da751-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da751-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da751-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da751-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da751-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da751-108">설명은</span><span class="sxs-lookup"><span data-stu-id="da751-108">DESCRIPTION</span></span>
<span data-ttu-id="da751-109">**AzIpAllocation** Cmdlet은 Azure ip 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="da751-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="da751-110">예제의</span><span class="sxs-lookup"><span data-stu-id="da751-110">EXAMPLES</span></span>

### <span data-ttu-id="da751-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="da751-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="da751-112">변수</span><span class="sxs-lookup"><span data-stu-id="da751-112">PARAMETERS</span></span>

### <span data-ttu-id="da751-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da751-113">-AsJob</span></span>
<span data-ttu-id="da751-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="da751-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da751-115">-DefaultProfile</span></span>
<span data-ttu-id="da751-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da751-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da751-117">-Force</span><span class="sxs-lookup"><span data-stu-id="da751-117">-Force</span></span>
<span data-ttu-id="da751-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da751-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="da751-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da751-119">-InputObject</span></span>
<span data-ttu-id="da751-120">{{Fill InputObject 설명}}</span><span class="sxs-lookup"><span data-stu-id="da751-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da751-121">-이름</span><span class="sxs-lookup"><span data-stu-id="da751-121">-Name</span></span>
<span data-ttu-id="da751-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da751-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da751-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da751-123">-PassThru</span></span>
<span data-ttu-id="da751-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="da751-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da751-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da751-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da751-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da751-126">-ResourceGroupName</span></span>
<span data-ttu-id="da751-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da751-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da751-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da751-128">-ResourceId</span></span>
<span data-ttu-id="da751-129">IpAllocation 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="da751-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da751-130">-확인</span><span class="sxs-lookup"><span data-stu-id="da751-130">-Confirm</span></span>
<span data-ttu-id="da751-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da751-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da751-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da751-132">-WhatIf</span></span>
<span data-ttu-id="da751-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da751-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da751-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da751-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da751-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da751-135">CommonParameters</span></span>
<span data-ttu-id="da751-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da751-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da751-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da751-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da751-138">입력</span><span class="sxs-lookup"><span data-stu-id="da751-138">INPUTS</span></span>

### <span data-ttu-id="da751-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da751-139">System.String</span></span>

## <span data-ttu-id="da751-140">출력</span><span class="sxs-lookup"><span data-stu-id="da751-140">OUTPUTS</span></span>

### <span data-ttu-id="da751-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="da751-141">System.Boolean</span></span>

## <span data-ttu-id="da751-142">상속자</span><span class="sxs-lookup"><span data-stu-id="da751-142">NOTES</span></span>

## <span data-ttu-id="da751-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da751-143">RELATED LINKS</span></span>
