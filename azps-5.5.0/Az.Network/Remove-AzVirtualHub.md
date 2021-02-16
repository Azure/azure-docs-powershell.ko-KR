---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186924"
---
# <span data-ttu-id="e97b4-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e97b4-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="e97b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e97b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e97b4-103">Azure VirtualHub 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e97b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="e97b4-104">SYNTAX</span></span>

### <span data-ttu-id="e97b4-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e97b4-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e97b4-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e97b4-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e97b4-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e97b4-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e97b4-108">설명</span><span class="sxs-lookup"><span data-stu-id="e97b4-108">DESCRIPTION</span></span>
<span data-ttu-id="e97b4-109">Azure VirtualHub 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e97b4-110">예제</span><span class="sxs-lookup"><span data-stu-id="e97b4-110">EXAMPLES</span></span>

### <span data-ttu-id="e97b4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e97b4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="e97b4-112">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e97b4-113">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e97b4-114">그런 다음 ResourceGroupName 및 ResourceName을 사용하여 가상 허브를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="e97b4-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="e97b4-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="e97b4-116">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e97b4-117">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e97b4-118">그런 다음 입력 개체를 사용하여 가상 허브를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="e97b4-119">입력 개체는 PSVirtualHub 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="e97b4-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="e97b4-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="e97b4-121">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e97b4-122">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e97b4-123">그런 다음 Get-AzVirtualHub의 출력을 사용하여 PowerShell 파이핑을 사용하여 가상 허브를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="e97b4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e97b4-124">PARAMETERS</span></span>

### <span data-ttu-id="e97b4-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e97b4-125">-AsJob</span></span>
<span data-ttu-id="e97b4-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e97b4-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e97b4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97b4-127">-DefaultProfile</span></span>
<span data-ttu-id="e97b4-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e97b4-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e97b4-129">-Force</span></span>
<span data-ttu-id="e97b4-130">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e97b4-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e97b4-131">-InputObject</span></span>
<span data-ttu-id="e97b4-132">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e97b4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e97b4-133">-Name</span></span>
<span data-ttu-id="e97b4-134">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e97b4-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e97b4-135">-PassThru</span></span>
<span data-ttu-id="e97b4-136">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e97b4-137">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e97b4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e97b4-138">-ResourceGroupName</span></span>
<span data-ttu-id="e97b4-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e97b4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e97b4-140">-ResourceId</span></span>
<span data-ttu-id="e97b4-141">수정할 가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97b4-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e97b4-142">-Confirm</span></span>
<span data-ttu-id="e97b4-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e97b4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e97b4-144">-WhatIf</span></span>
<span data-ttu-id="e97b4-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e97b4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e97b4-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e97b4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97b4-147">CommonParameters</span></span>
<span data-ttu-id="e97b4-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e97b4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97b4-149">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e97b4-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97b4-150">입력</span><span class="sxs-lookup"><span data-stu-id="e97b4-150">INPUTS</span></span>

### <span data-ttu-id="e97b4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e97b4-151">System.String</span></span>

### <span data-ttu-id="e97b4-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e97b4-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e97b4-153">출력</span><span class="sxs-lookup"><span data-stu-id="e97b4-153">OUTPUTS</span></span>

### <span data-ttu-id="e97b4-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e97b4-154">System.Boolean</span></span>

## <span data-ttu-id="e97b4-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e97b4-155">NOTES</span></span>

## <span data-ttu-id="e97b4-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e97b4-156">RELATED LINKS</span></span>

[<span data-ttu-id="e97b4-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e97b4-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="e97b4-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e97b4-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="e97b4-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e97b4-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
