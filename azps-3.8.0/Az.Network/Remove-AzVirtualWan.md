---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043963"
---
# <span data-ttu-id="befe4-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="befe4-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="befe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befe4-102">SYNOPSIS</span></span>
<span data-ttu-id="befe4-103">Azure 가상 WAN을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="befe4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="befe4-104">SYNTAX</span></span>

### <span data-ttu-id="befe4-105">ByVirtualWanName (기본값)</span><span class="sxs-lookup"><span data-stu-id="befe4-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="befe4-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="befe4-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="befe4-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="befe4-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="befe4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="befe4-108">DESCRIPTION</span></span>
<span data-ttu-id="befe4-109">Azure 가상 WAN을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="befe4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="befe4-110">EXAMPLES</span></span>

### <span data-ttu-id="befe4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="befe4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="befe4-112">이 예제에서는 리소스 그룹에 가상 WAN을 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="befe4-113">가상 WAN을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="befe4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="befe4-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="befe4-115">이 예제에서는 리소스 그룹에 가상 WAN을 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="befe4-116">이 삭제는 New-AzVirtualWan에서 반환 된 가상 wan 개체를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="befe4-117">가상 WAN을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="befe4-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="befe4-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="befe4-119">이 예제에서는 리소스 그룹에 가상 WAN을 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="befe4-120">이 삭제는 New-AzVirtualWan에서 반환 된 가상 wan 리소스 id를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="befe4-121">가상 WAN을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="befe4-122">변수</span><span class="sxs-lookup"><span data-stu-id="befe4-122">PARAMETERS</span></span>

### <span data-ttu-id="befe4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befe4-123">-DefaultProfile</span></span>
<span data-ttu-id="befe4-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="befe4-125">-Force</span><span class="sxs-lookup"><span data-stu-id="befe4-125">-Force</span></span>
<span data-ttu-id="befe4-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="befe4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="befe4-127">-InputObject</span></span>
<span data-ttu-id="befe4-128">삭제할 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="befe4-129">-이름</span><span class="sxs-lookup"><span data-stu-id="befe4-129">-Name</span></span>
<span data-ttu-id="befe4-130">가상 wan 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="befe4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="befe4-131">-PassThru</span></span>
<span data-ttu-id="befe4-132">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="befe4-133">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="befe4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befe4-134">-ResourceGroupName</span></span>
<span data-ttu-id="befe4-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-135">The resource group name.</span></span>

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

### <span data-ttu-id="befe4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="befe4-136">-ResourceId</span></span>
<span data-ttu-id="befe4-137">삭제할 가상 wan의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="befe4-138">-확인</span><span class="sxs-lookup"><span data-stu-id="befe4-138">-Confirm</span></span>
<span data-ttu-id="befe4-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="befe4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="befe4-140">-WhatIf</span></span>
<span data-ttu-id="befe4-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="befe4-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="befe4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befe4-143">CommonParameters</span></span>
<span data-ttu-id="befe4-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="befe4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befe4-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="befe4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befe4-146">입력</span><span class="sxs-lookup"><span data-stu-id="befe4-146">INPUTS</span></span>

### <span data-ttu-id="befe4-147">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="befe4-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="befe4-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="befe4-148">System.String</span></span>

## <span data-ttu-id="befe4-149">출력</span><span class="sxs-lookup"><span data-stu-id="befe4-149">OUTPUTS</span></span>

### <span data-ttu-id="befe4-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="befe4-150">System.Boolean</span></span>

## <span data-ttu-id="befe4-151">상속자</span><span class="sxs-lookup"><span data-stu-id="befe4-151">NOTES</span></span>

## <span data-ttu-id="befe4-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="befe4-152">RELATED LINKS</span></span>

[<span data-ttu-id="befe4-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="befe4-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="befe4-154">새로운 AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="befe4-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="befe4-155">업데이트-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="befe4-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
