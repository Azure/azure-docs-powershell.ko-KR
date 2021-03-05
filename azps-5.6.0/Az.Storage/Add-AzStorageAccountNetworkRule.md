---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976176"
---
# <span data-ttu-id="a8f8d-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8f8d-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="a8f8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8f8d-102">SYNOPSIS</span></span>
 <span data-ttu-id="a8f8d-103">Storage 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="a8f8d-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="a8f8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8f8d-104">SYNTAX</span></span>

### <span data-ttu-id="a8f8d-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="a8f8d-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f8d-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="a8f8d-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f8d-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="a8f8d-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f8d-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="a8f8d-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f8d-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="a8f8d-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f8d-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="a8f8d-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8f8d-111">설명</span><span class="sxs-lookup"><span data-stu-id="a8f8d-111">DESCRIPTION</span></span>
<span data-ttu-id="a8f8d-112">**Add-AzStorageAccountNetworkRule** cmdlet은 Storage 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="a8f8d-113">예제</span><span class="sxs-lookup"><span data-stu-id="a8f8d-113">EXAMPLES</span></span>

### <span data-ttu-id="a8f8d-114">예제 1: IPAddressOrRange를 통해 여러 IPRules 추가</span><span class="sxs-lookup"><span data-stu-id="a8f8d-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="a8f8d-115">이 명령은 IPAddressOrRange를 사용하여 여러 IPRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="a8f8d-116">예제 2: VirtualNetworkResourceID를 통해 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="a8f8d-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="a8f8d-117">이 명령은 VirtualNetworkResourceID를 사용하여 VirtualNetworkRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="a8f8d-118">예제 3: 다른 계정의 VirtualNetworkRule 개체로 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="a8f8d-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="a8f8d-119">이 명령은 다른 계정의 VirtualNetworkRule 개체로 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="a8f8d-120">예제 4: IpRule 개체로 여러 IpRule 추가, JSON을 사용하여 입력</span><span class="sxs-lookup"><span data-stu-id="a8f8d-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="a8f8d-121">이 명령은 IpRule 개체가 있는 여러 IpRule을 추가하고 JSON을 사용하여 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="a8f8d-122">예제 5: 리소스 액세스 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="a8f8d-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="a8f8d-123">이 명령은 TenantId 및 ResourceId를 사용하여 리소스 액세스 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="a8f8d-124">예제 6: 다른 저장소 계정에 하나의 저장소 계정의 모든 리소스 액세스 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="a8f8d-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="a8f8d-125">이 명령은 한 저장소 계정에서 모든 리소스 액세스 규칙을 얻게 하여 다른 저장소 계정에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="a8f8d-126">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a8f8d-126">PARAMETERS</span></span>

### <span data-ttu-id="a8f8d-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8f8d-127">-AsJob</span></span>
<span data-ttu-id="a8f8d-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a8f8d-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8f8d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f8d-129">-DefaultProfile</span></span>
<span data-ttu-id="a8f8d-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f8d-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a8f8d-131">-IPAddressOrRange</span></span>
<span data-ttu-id="a8f8d-132">IpAddressOrRange의 배열은 IpAddressOrRange 입력과 함께 IpRules를 추가하고 기본 작업 허용을 NetworkRule 속성에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="a8f8d-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="a8f8d-133">-IPRule</span></span>
<span data-ttu-id="a8f8d-134">NetworkRule 속성에 추가할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="a8f8d-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a8f8d-135">-Name</span></span>
<span data-ttu-id="a8f8d-136">Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="a8f8d-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="a8f8d-137">-ResourceAccessRule</span></span>
<span data-ttu-id="a8f8d-138">Storage 계정 NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="a8f8d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f8d-139">-ResourceGroupName</span></span>
<span data-ttu-id="a8f8d-140">리소스 그룹의 이름을 저장소 계정으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="a8f8d-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8f8d-141">-ResourceId</span></span>
<span data-ttu-id="a8f8d-142">String의 Storage 계정 ResourceAccessRule ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="a8f8d-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a8f8d-143">-TenantId</span></span>
<span data-ttu-id="a8f8d-144">String의 Storage 계정 ResourceAccessRule TenantId.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="a8f8d-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a8f8d-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a8f8d-146">VirtualNetworkResourceId의 배열은 VirtualNetworkResourceId 입력과 함께 VirtualNetworkRule을 추가하고 기본 작업 허용을 NetworkRule 속성에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="a8f8d-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8f8d-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="a8f8d-148">NetworkRule 속성에 추가할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="a8f8d-149">-확인</span><span class="sxs-lookup"><span data-stu-id="a8f8d-149">-Confirm</span></span>
<span data-ttu-id="a8f8d-150">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f8d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f8d-151">-WhatIf</span></span>
<span data-ttu-id="a8f8d-152">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8f8d-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f8d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f8d-154">CommonParameters</span></span>
<span data-ttu-id="a8f8d-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f8d-156">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a8f8d-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f8d-157">입력</span><span class="sxs-lookup"><span data-stu-id="a8f8d-157">INPUTS</span></span>

### <span data-ttu-id="a8f8d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a8f8d-158">System.String</span></span>

### <span data-ttu-id="a8f8d-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="a8f8d-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="a8f8d-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="a8f8d-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="a8f8d-161">출력</span><span class="sxs-lookup"><span data-stu-id="a8f8d-161">OUTPUTS</span></span>

### <span data-ttu-id="a8f8d-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8f8d-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="a8f8d-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="a8f8d-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="a8f8d-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8f8d-164">NOTES</span></span>

## <span data-ttu-id="a8f8d-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8f8d-165">RELATED LINKS</span></span>
