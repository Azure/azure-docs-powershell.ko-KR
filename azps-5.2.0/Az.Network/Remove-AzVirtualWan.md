---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370658"
---
# <span data-ttu-id="ae2b3-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="ae2b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2b3-103">Azure Virtual WAN을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="ae2b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae2b3-104">SYNTAX</span></span>

### <span data-ttu-id="ae2b3-105">ByVirtualWanName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ae2b3-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2b3-108">설명</span><span class="sxs-lookup"><span data-stu-id="ae2b3-108">DESCRIPTION</span></span>
<span data-ttu-id="ae2b3-109">Azure Virtual WAN을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="ae2b3-110">예제</span><span class="sxs-lookup"><span data-stu-id="ae2b3-110">EXAMPLES</span></span>

### <span data-ttu-id="ae2b3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae2b3-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="ae2b3-112">이 예제에서는 리소스 그룹에 Virtual WAN을 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="ae2b3-113">Virtual WAN을 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="ae2b3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ae2b3-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="ae2b3-115">이 예제에서는 리소스 그룹에 Virtual WAN을 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="ae2b3-116">이 삭제는 New-AzVirtualWan에서 반환된 가상 wan 개체를 사용하여 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="ae2b3-117">Virtual WAN을 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="ae2b3-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="ae2b3-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="ae2b3-119">이 예제에서는 리소스 그룹에 Virtual WAN을 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="ae2b3-120">이 지우는 New-AzVirtualWan에서 반환된 가상 wan 리소스 ID를 사용하여 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="ae2b3-121">Virtual WAN을 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="ae2b3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-122">PARAMETERS</span></span>

### <span data-ttu-id="ae2b3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2b3-123">-DefaultProfile</span></span>
<span data-ttu-id="ae2b3-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2b3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ae2b3-125">-Force</span></span>
<span data-ttu-id="ae2b3-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ae2b3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae2b3-127">-InputObject</span></span>
<span data-ttu-id="ae2b3-128">삭제할 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ae2b3-129">-Name</span></span>
<span data-ttu-id="ae2b3-130">가상 wan 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae2b3-131">-PassThru</span></span>
<span data-ttu-id="ae2b3-132">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae2b3-133">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae2b3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2b3-134">-ResourceGroupName</span></span>
<span data-ttu-id="ae2b3-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-136">-ResourceId</span></span>
<span data-ttu-id="ae2b3-137">삭제할 가상 wan에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae2b3-138">-Confirm</span></span>
<span data-ttu-id="ae2b3-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2b3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2b3-140">-WhatIf</span></span>
<span data-ttu-id="ae2b3-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ae2b3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae2b3-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2b3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2b3-143">CommonParameters</span></span>
<span data-ttu-id="ae2b3-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2b3-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2b3-146">입력</span><span class="sxs-lookup"><span data-stu-id="ae2b3-146">INPUTS</span></span>

### <span data-ttu-id="ae2b3-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="ae2b3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ae2b3-148">System.String</span></span>

## <span data-ttu-id="ae2b3-149">출력</span><span class="sxs-lookup"><span data-stu-id="ae2b3-149">OUTPUTS</span></span>

### <span data-ttu-id="ae2b3-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae2b3-150">System.Boolean</span></span>

## <span data-ttu-id="ae2b3-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae2b3-151">NOTES</span></span>

## <span data-ttu-id="ae2b3-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae2b3-152">RELATED LINKS</span></span>

[<span data-ttu-id="ae2b3-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="ae2b3-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="ae2b3-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
