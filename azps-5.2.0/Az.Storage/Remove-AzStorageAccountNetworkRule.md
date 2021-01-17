---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359073"
---
# <span data-ttu-id="24f8f-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="24f8f-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="24f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="24f8f-103">Storage 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="24f8f-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="24f8f-104">구문</span><span class="sxs-lookup"><span data-stu-id="24f8f-104">SYNTAX</span></span>

### <span data-ttu-id="24f8f-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="24f8f-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24f8f-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="24f8f-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f8f-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="24f8f-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f8f-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="24f8f-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f8f-109">설명</span><span class="sxs-lookup"><span data-stu-id="24f8f-109">DESCRIPTION</span></span>
<span data-ttu-id="24f8f-110">**Remove-AzStorageAccountNetworkRule** cmdlet은 Storage 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="24f8f-111">예제</span><span class="sxs-lookup"><span data-stu-id="24f8f-111">EXAMPLES</span></span>

### <span data-ttu-id="24f8f-112">예제 1: IPAddressOrRange를 사용하여 여러 IpRules 제거</span><span class="sxs-lookup"><span data-stu-id="24f8f-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="24f8f-113">이 명령은 IPAddressOrRange를 사용하여 여러 IpRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="24f8f-114">예제 2: JSON을 사용하여 VirtualNetworkRule 개체 입력으로 VirtualNetworkRule 제거</span><span class="sxs-lookup"><span data-stu-id="24f8f-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="24f8f-115">이 명령은 JSON을 사용하여 VirtualNetworkRule 개체 입력을 사용하여 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="24f8f-116">예제 3: 파이프라인을 사용하여 첫 번째 IpRule 제거</span><span class="sxs-lookup"><span data-stu-id="24f8f-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="24f8f-117">이 명령은 파이프라인이 있는 첫 번째 IpRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="24f8f-118">예제 4: VirtualNetworkResourceID를 사용하여 여러 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="24f8f-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="24f8f-119">이 명령은 VirtualNetworkResourceID를 사용하여 여러 VirtualNetworkRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="24f8f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24f8f-120">PARAMETERS</span></span>

### <span data-ttu-id="24f8f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f8f-121">-AsJob</span></span>
<span data-ttu-id="24f8f-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="24f8f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f8f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f8f-123">-DefaultProfile</span></span>
<span data-ttu-id="24f8f-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f8f-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="24f8f-125">-IPAddressOrRange</span></span>
<span data-ttu-id="24f8f-126">IpAddressOrRange의 배열은 NetWorkRule 속성에서 동일한 IpAddressOrRange를 사용하여 IpRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="24f8f-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="24f8f-127">-IPRule</span></span>
<span data-ttu-id="24f8f-128">NetWorkRule 속성에서 제거할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="24f8f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="24f8f-129">-Name</span></span>
<span data-ttu-id="24f8f-130">Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="24f8f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f8f-131">-ResourceGroupName</span></span>
<span data-ttu-id="24f8f-132">Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="24f8f-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="24f8f-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="24f8f-134">VirtualNetworkResourceId의 배열은 NetWorkRule 속성에서 VirtualNetworkResourceId와 동일한 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="24f8f-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="24f8f-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="24f8f-136">NetWorkRule 속성에서 제거할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="24f8f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24f8f-137">-Confirm</span></span>
<span data-ttu-id="24f8f-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f8f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f8f-139">-WhatIf</span></span>
<span data-ttu-id="24f8f-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="24f8f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f8f-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f8f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f8f-142">CommonParameters</span></span>
<span data-ttu-id="24f8f-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24f8f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f8f-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="24f8f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f8f-145">입력</span><span class="sxs-lookup"><span data-stu-id="24f8f-145">INPUTS</span></span>

### <span data-ttu-id="24f8f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="24f8f-146">System.String</span></span>

### <span data-ttu-id="24f8f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="24f8f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="24f8f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="24f8f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="24f8f-149">출력</span><span class="sxs-lookup"><span data-stu-id="24f8f-149">OUTPUTS</span></span>

### <span data-ttu-id="24f8f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="24f8f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="24f8f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="24f8f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="24f8f-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24f8f-152">NOTES</span></span>

## <span data-ttu-id="24f8f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24f8f-153">RELATED LINKS</span></span>
