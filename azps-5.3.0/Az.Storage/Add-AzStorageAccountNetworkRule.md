---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376370"
---
# <span data-ttu-id="2eb52-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2eb52-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="2eb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb52-102">SYNOPSIS</span></span>
 <span data-ttu-id="2eb52-103">Storage 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="2eb52-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="2eb52-104">구문</span><span class="sxs-lookup"><span data-stu-id="2eb52-104">SYNTAX</span></span>

### <span data-ttu-id="2eb52-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="2eb52-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2eb52-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="2eb52-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb52-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="2eb52-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb52-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="2eb52-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb52-109">설명</span><span class="sxs-lookup"><span data-stu-id="2eb52-109">DESCRIPTION</span></span>
<span data-ttu-id="2eb52-110">**Add-AzStorageAccountNetworkRule** cmdlet은 Storage 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="2eb52-111">예제</span><span class="sxs-lookup"><span data-stu-id="2eb52-111">EXAMPLES</span></span>

### <span data-ttu-id="2eb52-112">예제 1: IPAddressOrRange를 통해 여러 IpRules 추가</span><span class="sxs-lookup"><span data-stu-id="2eb52-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="2eb52-113">이 명령은 IPAddressOrRange를 사용하여 여러 IpRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="2eb52-114">예제 2: VirtualNetworkResourceID를 통해 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="2eb52-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="2eb52-115">이 명령은 VirtualNetworkResourceID를 사용하여 VirtualNetworkRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="2eb52-116">예제 3: 다른 계정에서 VirtualNetworkRule 개체를 사용하여 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="2eb52-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="2eb52-117">이 명령은 다른 계정의 VirtualNetworkRule 개체를 사용하여 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="2eb52-118">예제 4: JSON을 사용하여 입력한 IpRule 개체로 여러 IpRule 추가</span><span class="sxs-lookup"><span data-stu-id="2eb52-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="2eb52-119">이 명령은 JSON을 사용하여 입력한 IpRule 개체가 있는 여러 IpRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="2eb52-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb52-120">PARAMETERS</span></span>

### <span data-ttu-id="2eb52-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eb52-121">-AsJob</span></span>
<span data-ttu-id="2eb52-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2eb52-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2eb52-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb52-123">-DefaultProfile</span></span>
<span data-ttu-id="2eb52-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb52-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2eb52-125">-IPAddressOrRange</span></span>
<span data-ttu-id="2eb52-126">IpAddressOrRange의 배열로, 입력 IpAddressOrRange 및 NetworkRule 속성에 대한 기본 작업 허용을 사용하여 IpRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb52-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="2eb52-127">-IPRule</span></span>
<span data-ttu-id="2eb52-128">NetworkRule 속성에 추가할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb52-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb52-129">-Name</span></span>
<span data-ttu-id="2eb52-130">Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb52-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb52-131">-ResourceGroupName</span></span>
<span data-ttu-id="2eb52-132">Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb52-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb52-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="2eb52-134">VirtualNetworkResourceId의 배열은 VirtualNetworkResourceId 입력 및 NetworkRule 속성에 대한 기본 작업 허용을 사용하여 VirtualNetworkRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb52-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2eb52-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="2eb52-136">NetworkRule 속성에 추가할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb52-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eb52-137">-Confirm</span></span>
<span data-ttu-id="2eb52-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb52-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb52-139">-WhatIf</span></span>
<span data-ttu-id="2eb52-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2eb52-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb52-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb52-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb52-142">CommonParameters</span></span>
<span data-ttu-id="2eb52-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb52-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb52-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2eb52-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb52-145">입력</span><span class="sxs-lookup"><span data-stu-id="2eb52-145">INPUTS</span></span>

### <span data-ttu-id="2eb52-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2eb52-146">System.String</span></span>

### <span data-ttu-id="2eb52-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="2eb52-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="2eb52-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="2eb52-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="2eb52-149">출력</span><span class="sxs-lookup"><span data-stu-id="2eb52-149">OUTPUTS</span></span>

### <span data-ttu-id="2eb52-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2eb52-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="2eb52-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="2eb52-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="2eb52-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2eb52-152">NOTES</span></span>

## <span data-ttu-id="2eb52-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2eb52-153">RELATED LINKS</span></span>
