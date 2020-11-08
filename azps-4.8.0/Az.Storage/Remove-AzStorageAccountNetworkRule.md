---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048587"
---
# <span data-ttu-id="1d8e0-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8e0-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="1d8e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8e0-103">저장소 계정의 네트워크 규칙 속성에서 IpRules 또는 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="1d8e0-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="1d8e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d8e0-104">SYNTAX</span></span>

### <span data-ttu-id="1d8e0-105">NetWorkRuleString (기본값)</span><span class="sxs-lookup"><span data-stu-id="1d8e0-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d8e0-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d8e0-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8e0-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d8e0-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8e0-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="1d8e0-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8e0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1d8e0-109">DESCRIPTION</span></span>
<span data-ttu-id="1d8e0-110">AzStorageAccountNetworkRule cmdlet이 저장소 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="1d8e0-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="1d8e0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1d8e0-111">EXAMPLES</span></span>

### <span data-ttu-id="1d8e0-112">예제 1: IPAddressOrRange를 사용 하 여 여러 IpRules 제거</span><span class="sxs-lookup"><span data-stu-id="1d8e0-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="1d8e0-113">이 명령은 IPAddressOrRange로 여러 IpRules를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="1d8e0-114">예제 2: JSON을 사용 하 여 VirtualNetworkRule 개체 입력을 사용 하 여 VirtualNetworkRule 제거</span><span class="sxs-lookup"><span data-stu-id="1d8e0-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="1d8e0-115">이 명령은 JSON에서 VirtualNetworkRule 개체 입력을 사용 하 여 VirtualNetworkRule를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="1d8e0-116">예제 3: 파이프라인을 사용 하 여 첫 번째 IpRule 제거</span><span class="sxs-lookup"><span data-stu-id="1d8e0-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="1d8e0-117">이 명령은 파이프라인을 사용 하 여 첫 번째 IpRule를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="1d8e0-118">예제 4: VirtualNetworkResourceID를 사용 하 여 여러 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="1d8e0-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="1d8e0-119">이 명령은 VirtualNetworkResourceID로 여러 VirtualNetworkRules를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="1d8e0-120">변수</span><span class="sxs-lookup"><span data-stu-id="1d8e0-120">PARAMETERS</span></span>

### <span data-ttu-id="1d8e0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d8e0-121">-AsJob</span></span>
<span data-ttu-id="1d8e0-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1d8e0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d8e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8e0-123">-DefaultProfile</span></span>
<span data-ttu-id="1d8e0-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d8e0-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1d8e0-125">-IPAddressOrRange</span></span>
<span data-ttu-id="1d8e0-126">IpAddressOrRange의 배열은 NetWorkRule 속성과 동일한 IpAddressOrRange의 IpRule를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="1d8e0-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1d8e0-127">-IPRule</span></span>
<span data-ttu-id="1d8e0-128">NetWorkRule 속성에서 제거할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="1d8e0-129">-이름</span><span class="sxs-lookup"><span data-stu-id="1d8e0-129">-Name</span></span>
<span data-ttu-id="1d8e0-130">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="1d8e0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8e0-131">-ResourceGroupName</span></span>
<span data-ttu-id="1d8e0-132">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1d8e0-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1d8e0-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1d8e0-134">VirtualNetworkResourceId의 배열은 NetWorkRule 속성과 동일한 VirtualNetworkResourceId의 VirtualNetworkRule를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="1d8e0-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8e0-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="1d8e0-136">NetWorkRule 속성에서 제거할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="1d8e0-137">-확인</span><span class="sxs-lookup"><span data-stu-id="1d8e0-137">-Confirm</span></span>
<span data-ttu-id="1d8e0-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8e0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8e0-139">-WhatIf</span></span>
<span data-ttu-id="1d8e0-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8e0-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8e0-142">CommonParameters</span></span>
<span data-ttu-id="1d8e0-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8e0-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d8e0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8e0-145">입력</span><span class="sxs-lookup"><span data-stu-id="1d8e0-145">INPUTS</span></span>

### <span data-ttu-id="1d8e0-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1d8e0-146">System.String</span></span>

### <span data-ttu-id="1d8e0-147">PSIpRule []를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1d8e0-148">PSVirtualNetworkRule []를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1d8e0-149">출력</span><span class="sxs-lookup"><span data-stu-id="1d8e0-149">OUTPUTS</span></span>

### <span data-ttu-id="1d8e0-150">PSVirtualNetworkRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="1d8e0-151">PSIpRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8e0-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="1d8e0-152">상속자</span><span class="sxs-lookup"><span data-stu-id="1d8e0-152">NOTES</span></span>

## <span data-ttu-id="1d8e0-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d8e0-153">RELATED LINKS</span></span>
