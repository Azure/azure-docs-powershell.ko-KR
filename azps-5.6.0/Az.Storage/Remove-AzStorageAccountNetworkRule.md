---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973328"
---
# <span data-ttu-id="44361-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="44361-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="44361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44361-102">SYNOPSIS</span></span>
<span data-ttu-id="44361-103">Storage 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="44361-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="44361-104">구문</span><span class="sxs-lookup"><span data-stu-id="44361-104">SYNTAX</span></span>

### <span data-ttu-id="44361-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="44361-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44361-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="44361-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44361-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="44361-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44361-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="44361-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44361-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="44361-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44361-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="44361-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44361-111">설명</span><span class="sxs-lookup"><span data-stu-id="44361-111">DESCRIPTION</span></span>
<span data-ttu-id="44361-112">**Remove-AzStorageAccountNetworkRule** cmdlet은 Storage 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="44361-113">예제</span><span class="sxs-lookup"><span data-stu-id="44361-113">EXAMPLES</span></span>

### <span data-ttu-id="44361-114">예제 1: IPAddressOrRange를 사용하여 여러 IPRules 제거</span><span class="sxs-lookup"><span data-stu-id="44361-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="44361-115">이 명령은 IPAddressOrRange를 사용하여 여러 IPRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="44361-116">예제 2: JSON을 사용하여 VirtualNetworkRule 개체 입력으로 VirtualNetworkRule 제거</span><span class="sxs-lookup"><span data-stu-id="44361-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="44361-117">이 명령은 JSON을 사용하여 VirtualNetworkRule 개체 입력을 사용하여 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="44361-118">예제 3: 파이프라인을 사용하여 첫 번째 IpRule 제거</span><span class="sxs-lookup"><span data-stu-id="44361-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="44361-119">이 명령은 파이프라인을 사용하여 첫 번째 IpRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="44361-120">예제 4: VirtualNetworkResourceID를 사용하여 여러 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="44361-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="44361-121">이 명령은 VirtualNetworkResourceID를 사용하여 여러 VirtualNetworkRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="44361-122">예제 5: TenantId 및 ResourceId를 사용하여 리소스 액세스 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="44361-123">이 명령은 TenantId 및 ResourceId를 사용하여 리소스 액세스 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="44361-124">예제 6: 저장소 계정에서 처음 3개 리소스 액세스 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="44361-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="44361-125">이 명령은 저장소 계정에서 처음 3개 리소스 액세스 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="44361-126">매개 변수</span><span class="sxs-lookup"><span data-stu-id="44361-126">PARAMETERS</span></span>

### <span data-ttu-id="44361-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44361-127">-AsJob</span></span>
<span data-ttu-id="44361-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="44361-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44361-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44361-129">-DefaultProfile</span></span>
<span data-ttu-id="44361-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44361-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44361-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="44361-131">-IPAddressOrRange</span></span>
<span data-ttu-id="44361-132">IpAddressOrRange의 배열은 NetWorkRule 속성에서 동일한 IpAddressOrRange를 사용하여 IpRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="44361-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="44361-133">-IPRule</span></span>
<span data-ttu-id="44361-134">NetWorkRule 속성에서 제거할 IpRule 개체 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="44361-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="44361-135">-Name</span><span class="sxs-lookup"><span data-stu-id="44361-135">-Name</span></span>
<span data-ttu-id="44361-136">Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="44361-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="44361-137">-ResourceAccessRule</span></span>
<span data-ttu-id="44361-138">Storage 계정 NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="44361-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44361-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44361-139">-ResourceGroupName</span></span>
<span data-ttu-id="44361-140">리소스 그룹의 이름을 저장소 계정으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="44361-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44361-141">-ResourceId</span></span>
<span data-ttu-id="44361-142">String의 Storage 계정 ResourceAccessRule ResourceId.</span><span class="sxs-lookup"><span data-stu-id="44361-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44361-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="44361-143">-TenantId</span></span>
<span data-ttu-id="44361-144">String의 Storage 계정 ResourceAccessRule TenantId.</span><span class="sxs-lookup"><span data-stu-id="44361-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44361-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="44361-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="44361-146">VirtualNetworkResourceId의 배열은 NetWorkRule 속성에서 동일한 VirtualNetworkResourceId를 사용하여 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="44361-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="44361-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="44361-148">NetWorkRule 속성에서 제거할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="44361-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="44361-149">-확인</span><span class="sxs-lookup"><span data-stu-id="44361-149">-Confirm</span></span>
<span data-ttu-id="44361-150">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44361-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44361-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44361-151">-WhatIf</span></span>
<span data-ttu-id="44361-152">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="44361-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44361-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44361-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44361-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44361-154">CommonParameters</span></span>
<span data-ttu-id="44361-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44361-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44361-156">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44361-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44361-157">입력</span><span class="sxs-lookup"><span data-stu-id="44361-157">INPUTS</span></span>

### <span data-ttu-id="44361-158">System.String</span><span class="sxs-lookup"><span data-stu-id="44361-158">System.String</span></span>

### <span data-ttu-id="44361-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="44361-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="44361-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="44361-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="44361-161">출력</span><span class="sxs-lookup"><span data-stu-id="44361-161">OUTPUTS</span></span>

### <span data-ttu-id="44361-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="44361-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="44361-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="44361-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="44361-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44361-164">NOTES</span></span>

## <span data-ttu-id="44361-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44361-165">RELATED LINKS</span></span>
