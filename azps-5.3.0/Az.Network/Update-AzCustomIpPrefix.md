---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490924"
---
# <span data-ttu-id="7c9d3-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7c9d3-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="7c9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9d3-103">CustomIpPrefix 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c9d3-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="7c9d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c9d3-104">SYNTAX</span></span>

### <span data-ttu-id="7c9d3-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9d3-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c9d3-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9d3-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9d3-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9d3-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9d3-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c9d3-108">DESCRIPTION</span></span>
<span data-ttu-id="7c9d3-109">**Update-AzCustomIpPrefix** cmdlet을 사용하면 사용자가 CustomIpPrefix를 커미션하거나 해제하거나 리소스의 태그를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="7c9d3-110">예제</span><span class="sxs-lookup"><span data-stu-id="7c9d3-110">EXAMPLES</span></span>

### <span data-ttu-id="7c9d3-111">예제 1: CustomIpPrefix 위임</span><span class="sxs-lookup"><span data-stu-id="7c9d3-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="7c9d3-112">위의 명령은 CustomIpPrefix의 위임 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="7c9d3-113">예제 2: CustomIpPrefix 해제</span><span class="sxs-lookup"><span data-stu-id="7c9d3-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="7c9d3-114">위의 명령은 CustomIpPrefix의 위임 위임 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="7c9d3-115">예제 3: CustomIpPrefix에 대한 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c9d3-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="7c9d3-116">위의 명령은 CustomIpPrefix에 대한 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="7c9d3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c9d3-117">PARAMETERS</span></span>

### <span data-ttu-id="7c9d3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c9d3-118">-AsJob</span></span>
<span data-ttu-id="7c9d3-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c9d3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c9d3-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="7c9d3-120">-Commission</span></span>
<span data-ttu-id="7c9d3-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c9d3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c9d3-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="7c9d3-122">-Decomission</span></span>
<span data-ttu-id="7c9d3-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c9d3-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c9d3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9d3-124">-DefaultProfile</span></span>
<span data-ttu-id="7c9d3-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c9d3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c9d3-126">-InputObject</span></span>
<span data-ttu-id="7c9d3-127">설정할 CustomIpPrefix입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9d3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7c9d3-128">-Name</span></span>
<span data-ttu-id="7c9d3-129">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c9d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="7c9d3-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9d3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c9d3-132">-ResourceId</span></span>
<span data-ttu-id="7c9d3-133">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9d3-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c9d3-134">-Tag</span></span>
<span data-ttu-id="7c9d3-135">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9d3-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c9d3-136">-Confirm</span></span>
<span data-ttu-id="7c9d3-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c9d3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9d3-138">-WhatIf</span></span>
<span data-ttu-id="7c9d3-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7c9d3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c9d3-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c9d3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9d3-141">CommonParameters</span></span>
<span data-ttu-id="7c9d3-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9d3-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9d3-144">입력</span><span class="sxs-lookup"><span data-stu-id="7c9d3-144">INPUTS</span></span>

### <span data-ttu-id="7c9d3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7c9d3-145">System.String</span></span>

### <span data-ttu-id="7c9d3-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7c9d3-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="7c9d3-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c9d3-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c9d3-148">출력</span><span class="sxs-lookup"><span data-stu-id="7c9d3-148">OUTPUTS</span></span>

### <span data-ttu-id="7c9d3-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7c9d3-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="7c9d3-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c9d3-150">NOTES</span></span>

## <span data-ttu-id="7c9d3-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c9d3-151">RELATED LINKS</span></span>

[<span data-ttu-id="7c9d3-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7c9d3-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="7c9d3-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7c9d3-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="7c9d3-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7c9d3-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)