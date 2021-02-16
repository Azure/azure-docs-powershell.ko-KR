---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186940"
---
# <span data-ttu-id="6b2be-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b2be-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="6b2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b2be-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2be-103">공용 IP 주소 제거</span><span class="sxs-lookup"><span data-stu-id="6b2be-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="6b2be-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b2be-104">SYNTAX</span></span>

### <span data-ttu-id="6b2be-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6b2be-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b2be-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b2be-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b2be-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b2be-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b2be-108">설명</span><span class="sxs-lookup"><span data-stu-id="6b2be-108">DESCRIPTION</span></span>
<span data-ttu-id="6b2be-109">**Remove-AzPublicIpPrefix** cmdlet은 할당된 공용 IP 주소가 없는 한 Azure 공용 IP 주소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="6b2be-110">예제</span><span class="sxs-lookup"><span data-stu-id="6b2be-110">EXAMPLES</span></span>

### <span data-ttu-id="6b2be-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b2be-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="6b2be-112">리소스 그룹에서 이름 지정이 있는 공용 IP $prefixName 제거합니다$rgName</span><span class="sxs-lookup"><span data-stu-id="6b2be-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="6b2be-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b2be-113">PARAMETERS</span></span>

### <span data-ttu-id="6b2be-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b2be-114">-AsJob</span></span>
<span data-ttu-id="6b2be-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6b2be-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b2be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2be-116">-DefaultProfile</span></span>
<span data-ttu-id="6b2be-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b2be-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6b2be-118">-Force</span></span>
<span data-ttu-id="6b2be-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6b2be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b2be-120">-InputObject</span></span>
<span data-ttu-id="6b2be-121">PublicIpPrefix 개체</span><span class="sxs-lookup"><span data-stu-id="6b2be-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2be-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b2be-122">-Name</span></span>
<span data-ttu-id="6b2be-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2be-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b2be-124">-PassThru</span></span>
<span data-ttu-id="6b2be-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6b2be-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b2be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b2be-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b2be-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2be-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b2be-129">-ResourceId</span></span>
<span data-ttu-id="6b2be-130">제거할 리소스의 resourceId</span><span class="sxs-lookup"><span data-stu-id="6b2be-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="6b2be-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b2be-131">-Confirm</span></span>
<span data-ttu-id="6b2be-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b2be-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2be-133">-WhatIf</span></span>
<span data-ttu-id="6b2be-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6b2be-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b2be-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b2be-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2be-136">CommonParameters</span></span>
<span data-ttu-id="6b2be-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b2be-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2be-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6b2be-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2be-139">입력</span><span class="sxs-lookup"><span data-stu-id="6b2be-139">INPUTS</span></span>

### <span data-ttu-id="6b2be-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6b2be-140">System.String</span></span>

### <span data-ttu-id="6b2be-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b2be-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="6b2be-142">출력</span><span class="sxs-lookup"><span data-stu-id="6b2be-142">OUTPUTS</span></span>

### <span data-ttu-id="6b2be-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b2be-143">System.Boolean</span></span>

## <span data-ttu-id="6b2be-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b2be-144">NOTES</span></span>

## <span data-ttu-id="6b2be-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b2be-145">RELATED LINKS</span></span>

[<span data-ttu-id="6b2be-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b2be-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="6b2be-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b2be-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="6b2be-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b2be-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
