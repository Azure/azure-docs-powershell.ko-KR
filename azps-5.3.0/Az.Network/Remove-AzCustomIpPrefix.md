---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490943"
---
# <span data-ttu-id="02a5e-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="02a5e-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="02a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="02a5e-103">CustomIpPrefix를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="02a5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="02a5e-104">SYNTAX</span></span>

### <span data-ttu-id="02a5e-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="02a5e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a5e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a5e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a5e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a5e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a5e-108">설명</span><span class="sxs-lookup"><span data-stu-id="02a5e-108">DESCRIPTION</span></span>
<span data-ttu-id="02a5e-109">**Remove-AzCustomIpPrefix** cmdlet은 CustomIpPrefix를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="02a5e-110">예제</span><span class="sxs-lookup"><span data-stu-id="02a5e-110">EXAMPLES</span></span>

### <span data-ttu-id="02a5e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="02a5e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="02a5e-112">리소스 그룹에서 이름 및 이름 $prefixName CustomIpPrefix를 제거합니다$rgName</span><span class="sxs-lookup"><span data-stu-id="02a5e-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="02a5e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a5e-113">PARAMETERS</span></span>

### <span data-ttu-id="02a5e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02a5e-114">-AsJob</span></span>
<span data-ttu-id="02a5e-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="02a5e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02a5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a5e-116">-DefaultProfile</span></span>
<span data-ttu-id="02a5e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a5e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="02a5e-118">-Force</span></span>
<span data-ttu-id="02a5e-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02a5e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02a5e-120">-InputObject</span></span>
<span data-ttu-id="02a5e-121">customIpPrefix 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02a5e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="02a5e-122">-Name</span></span>
<span data-ttu-id="02a5e-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a5e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02a5e-124">-PassThru</span></span>
<span data-ttu-id="02a5e-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02a5e-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02a5e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a5e-127">-ResourceGroupName</span></span>
<span data-ttu-id="02a5e-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a5e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02a5e-129">-ResourceId</span></span>
<span data-ttu-id="02a5e-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a5e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a5e-131">-Confirm</span></span>
<span data-ttu-id="02a5e-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a5e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a5e-133">-WhatIf</span></span>
<span data-ttu-id="02a5e-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="02a5e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a5e-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a5e-136">CommonParameters</span></span>
<span data-ttu-id="02a5e-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02a5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a5e-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02a5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a5e-139">입력</span><span class="sxs-lookup"><span data-stu-id="02a5e-139">INPUTS</span></span>

### <span data-ttu-id="02a5e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="02a5e-140">System.String</span></span>

### <span data-ttu-id="02a5e-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="02a5e-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="02a5e-142">출력</span><span class="sxs-lookup"><span data-stu-id="02a5e-142">OUTPUTS</span></span>

### <span data-ttu-id="02a5e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02a5e-143">System.Boolean</span></span>

## <span data-ttu-id="02a5e-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02a5e-144">NOTES</span></span>

## <span data-ttu-id="02a5e-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02a5e-145">RELATED LINKS</span></span>

[<span data-ttu-id="02a5e-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="02a5e-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="02a5e-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="02a5e-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="02a5e-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="02a5e-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)