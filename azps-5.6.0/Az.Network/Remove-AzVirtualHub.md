---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 7a5724346f1b94af0dbc07df16f9cdab5f798523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006112"
---
# <span data-ttu-id="218a1-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="218a1-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="218a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="218a1-102">SYNOPSIS</span></span>
<span data-ttu-id="218a1-103">Azure VirtualHub 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="218a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="218a1-104">SYNTAX</span></span>

### <span data-ttu-id="218a1-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="218a1-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="218a1-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="218a1-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="218a1-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="218a1-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="218a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="218a1-108">DESCRIPTION</span></span>
<span data-ttu-id="218a1-109">Azure VirtualHub 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="218a1-110">예제</span><span class="sxs-lookup"><span data-stu-id="218a1-110">EXAMPLES</span></span>

### <span data-ttu-id="218a1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="218a1-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="218a1-112">위의 리소스 그룹 "testRG", Virtual WAN 및 Azure의 해당 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="218a1-113">가상 허브에는 주소 공간이 "10.0.1.0/24"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="218a1-114">그런 다음 ResourceGroupName 및 ResourceName을 사용하여 가상 허브를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="218a1-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="218a1-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="218a1-116">위의 리소스 그룹 "testRG", Virtual WAN 및 Azure의 해당 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="218a1-117">가상 허브에는 주소 공간이 "10.0.1.0/24"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="218a1-118">그런 다음 입력 개체를 사용하여 가상 허브를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="218a1-119">입력 개체는 PSVirtualHub 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="218a1-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="218a1-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="218a1-121">위의 리소스 그룹 "testRG", Virtual WAN 및 Azure의 해당 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="218a1-122">가상 허브에는 주소 공간이 "10.0.1.0/24"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="218a1-123">그런 다음 Get-AzVirtualHub의 출력을 사용하여 powershell 배관을 사용하여 가상 허브를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="218a1-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="218a1-124">PARAMETERS</span></span>

### <span data-ttu-id="218a1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="218a1-125">-AsJob</span></span>
<span data-ttu-id="218a1-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="218a1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="218a1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218a1-127">-DefaultProfile</span></span>
<span data-ttu-id="218a1-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="218a1-129">-Force</span><span class="sxs-lookup"><span data-stu-id="218a1-129">-Force</span></span>
<span data-ttu-id="218a1-130">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="218a1-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="218a1-131">-InputObject</span></span>
<span data-ttu-id="218a1-132">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="218a1-133">-Name</span><span class="sxs-lookup"><span data-stu-id="218a1-133">-Name</span></span>
<span data-ttu-id="218a1-134">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-134">The resource name.</span></span>

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

### <span data-ttu-id="218a1-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="218a1-135">-PassThru</span></span>
<span data-ttu-id="218a1-136">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="218a1-137">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="218a1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218a1-138">-ResourceGroupName</span></span>
<span data-ttu-id="218a1-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-139">The resource group name.</span></span>

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

### <span data-ttu-id="218a1-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="218a1-140">-ResourceId</span></span>
<span data-ttu-id="218a1-141">수정할 가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="218a1-142">-확인</span><span class="sxs-lookup"><span data-stu-id="218a1-142">-Confirm</span></span>
<span data-ttu-id="218a1-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="218a1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218a1-144">-WhatIf</span></span>
<span data-ttu-id="218a1-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="218a1-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="218a1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218a1-147">CommonParameters</span></span>
<span data-ttu-id="218a1-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="218a1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218a1-149">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="218a1-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218a1-150">입력</span><span class="sxs-lookup"><span data-stu-id="218a1-150">INPUTS</span></span>

### <span data-ttu-id="218a1-151">System.String</span><span class="sxs-lookup"><span data-stu-id="218a1-151">System.String</span></span>

### <span data-ttu-id="218a1-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="218a1-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="218a1-153">출력</span><span class="sxs-lookup"><span data-stu-id="218a1-153">OUTPUTS</span></span>

### <span data-ttu-id="218a1-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="218a1-154">System.Boolean</span></span>

## <span data-ttu-id="218a1-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="218a1-155">NOTES</span></span>

## <span data-ttu-id="218a1-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="218a1-156">RELATED LINKS</span></span>

[<span data-ttu-id="218a1-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="218a1-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="218a1-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="218a1-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="218a1-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="218a1-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
