---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179452"
---
# <span data-ttu-id="8e072-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8e072-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="8e072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e072-102">SYNOPSIS</span></span>
<span data-ttu-id="8e072-103">가상 네트워크 탭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="8e072-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e072-104">SYNTAX</span></span>

### <span data-ttu-id="8e072-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8e072-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e072-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e072-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e072-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e072-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e072-108">설명</span><span class="sxs-lookup"><span data-stu-id="8e072-108">DESCRIPTION</span></span>
<span data-ttu-id="8e072-109">**Remove-AzVirtualNetworkTap** cmdlet은 Azure 가상 네트워크 탭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="8e072-110">예제</span><span class="sxs-lookup"><span data-stu-id="8e072-110">EXAMPLES</span></span>

### <span data-ttu-id="8e072-111">예제 1: 가상 네트워크 탭 제거</span><span class="sxs-lookup"><span data-stu-id="8e072-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="8e072-112">이 명령은 리소스 그룹 ResourceGroup1에서 VirtualNetworkTap1을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="8e072-113">Force *매개* 변수가 사용되지 않는 경우 사용자에게 이 작업을 확인하라는 메시지가 표시될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="8e072-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e072-114">PARAMETERS</span></span>

### <span data-ttu-id="8e072-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e072-115">-AsJob</span></span>
<span data-ttu-id="8e072-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8e072-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e072-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e072-117">-DefaultProfile</span></span>
<span data-ttu-id="8e072-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e072-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e072-119">-Force</span></span>
<span data-ttu-id="8e072-120">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8e072-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e072-121">-InputObject</span></span>
<span data-ttu-id="8e072-122">VirtualNetworkTap 리소스에 대한 참조</span><span class="sxs-lookup"><span data-stu-id="8e072-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e072-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8e072-123">-Name</span></span>
<span data-ttu-id="8e072-124">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-124">The name of the tap.</span></span>

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

### <span data-ttu-id="8e072-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e072-125">-PassThru</span></span>
<span data-ttu-id="8e072-126">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8e072-127">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8e072-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e072-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e072-129">가상 네트워크 탭의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="8e072-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e072-130">-ResourceId</span></span>
<span data-ttu-id="8e072-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="8e072-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="8e072-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e072-132">-Confirm</span></span>
<span data-ttu-id="8e072-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e072-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e072-134">-WhatIf</span></span>
<span data-ttu-id="8e072-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8e072-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e072-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e072-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e072-137">CommonParameters</span></span>
<span data-ttu-id="8e072-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e072-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e072-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e072-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e072-140">입력</span><span class="sxs-lookup"><span data-stu-id="8e072-140">INPUTS</span></span>

### <span data-ttu-id="8e072-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8e072-141">System.String</span></span>

### <span data-ttu-id="8e072-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8e072-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8e072-143">출력</span><span class="sxs-lookup"><span data-stu-id="8e072-143">OUTPUTS</span></span>

### <span data-ttu-id="8e072-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e072-144">System.Boolean</span></span>

## <span data-ttu-id="8e072-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e072-145">NOTES</span></span>

## <span data-ttu-id="8e072-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e072-146">RELATED LINKS</span></span>

[<span data-ttu-id="8e072-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8e072-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="8e072-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8e072-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="8e072-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8e072-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
