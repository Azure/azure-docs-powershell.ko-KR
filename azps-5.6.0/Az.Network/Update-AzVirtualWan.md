---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: eb6611bef2499c9aaf164ddbe2e7a31c63051751
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951472"
---
# <span data-ttu-id="51db1-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="51db1-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="51db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51db1-102">SYNOPSIS</span></span>
<span data-ttu-id="51db1-103">Azure Virtual WAN을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="51db1-104">구문</span><span class="sxs-lookup"><span data-stu-id="51db1-104">SYNTAX</span></span>

### <span data-ttu-id="51db1-105">ByVirtualWanName(기본값)</span><span class="sxs-lookup"><span data-stu-id="51db1-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51db1-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="51db1-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51db1-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="51db1-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51db1-108">설명</span><span class="sxs-lookup"><span data-stu-id="51db1-108">DESCRIPTION</span></span>
<span data-ttu-id="51db1-109">Azure Virtual WAN을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="51db1-110">예제</span><span class="sxs-lookup"><span data-stu-id="51db1-110">EXAMPLES</span></span>

### <span data-ttu-id="51db1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="51db1-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="51db1-112">위의 리소스 그룹은 "미국 서부"에 리소스 그룹 "testRG"를 만들고 Azure의 해당 리소스 그룹에 Azure Virtual WAN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="51db1-113">VirtualWan은 새 속성으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="51db1-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51db1-114">PARAMETERS</span></span>

### <span data-ttu-id="51db1-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="51db1-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="51db1-116">VirtualWan에 대한 분기 트래픽에 분기할 수 있도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="51db1-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="51db1-118">VirtualWan에 대한 vnet 트래픽에 vnet을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51db1-119">-AsJob</span></span>
<span data-ttu-id="51db1-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="51db1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51db1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51db1-121">-DefaultProfile</span></span>
<span data-ttu-id="51db1-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51db1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="51db1-123">-Force</span></span>
<span data-ttu-id="51db1-124">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="51db1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51db1-125">-InputObject</span></span>
<span data-ttu-id="51db1-126">수정할 가상 wan 개체</span><span class="sxs-lookup"><span data-stu-id="51db1-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="51db1-127">-Name</span></span>
<span data-ttu-id="51db1-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51db1-129">-ResourceGroupName</span></span>
<span data-ttu-id="51db1-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51db1-131">-ResourceId</span></span>
<span data-ttu-id="51db1-132">가상 wan에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="51db1-133">-Tag</span></span>
<span data-ttu-id="51db1-134">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="51db1-135">-VirtualWANType</span></span>
<span data-ttu-id="51db1-136">Virtual Wan의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db1-137">-확인</span><span class="sxs-lookup"><span data-stu-id="51db1-137">-Confirm</span></span>
<span data-ttu-id="51db1-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51db1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51db1-139">-WhatIf</span></span>
<span data-ttu-id="51db1-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51db1-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51db1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51db1-142">CommonParameters</span></span>
<span data-ttu-id="51db1-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51db1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51db1-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51db1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51db1-145">입력</span><span class="sxs-lookup"><span data-stu-id="51db1-145">INPUTS</span></span>

### <span data-ttu-id="51db1-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="51db1-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="51db1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="51db1-147">System.String</span></span>

## <span data-ttu-id="51db1-148">출력</span><span class="sxs-lookup"><span data-stu-id="51db1-148">OUTPUTS</span></span>

### <span data-ttu-id="51db1-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="51db1-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="51db1-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51db1-150">NOTES</span></span>

## <span data-ttu-id="51db1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51db1-151">RELATED LINKS</span></span>

[<span data-ttu-id="51db1-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="51db1-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="51db1-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="51db1-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="51db1-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="51db1-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
