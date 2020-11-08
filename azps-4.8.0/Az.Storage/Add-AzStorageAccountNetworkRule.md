---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056928"
---
# <span data-ttu-id="ccf20-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ccf20-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="ccf20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf20-102">SYNOPSIS</span></span>
 <span data-ttu-id="ccf20-103">저장소 계정의 네트워크 규칙 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="ccf20-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ccf20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccf20-104">SYNTAX</span></span>

### <span data-ttu-id="ccf20-105">NetWorkRuleString (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccf20-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccf20-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ccf20-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf20-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ccf20-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf20-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ccf20-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf20-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ccf20-109">DESCRIPTION</span></span>
<span data-ttu-id="ccf20-110">**추가-AzStorageAccountNetworkRule** Cmdlet은 저장소 계정의 networkrule 속성에 IpRules 또는 VirtualNetworkRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ccf20-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ccf20-111">EXAMPLES</span></span>

### <span data-ttu-id="ccf20-112">예제 1: IPAddressOrRange를 사용 하 여 여러 IpRules 추가</span><span class="sxs-lookup"><span data-stu-id="ccf20-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="ccf20-113">이 명령은 IPAddressOrRange로 여러 IpRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="ccf20-114">예제 2: VirtualNetworkResourceID를 사용 하 여 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="ccf20-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="ccf20-115">이 명령은 VirtualNetworkResourceID를 사용 하 여 VirtualNetworkRule를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="ccf20-116">예제 3: 다른 계정의 VirtualNetworkRule 개체를 사용 하 여 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="ccf20-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="ccf20-117">이 명령은 다른 계정의 VirtualNetworkRule 개체를 사용 하 여 VirtualNetworkRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="ccf20-118">예제 4: IpRule 개체를 사용 하 여 여러 IpRule 추가, JSON으로 입력</span><span class="sxs-lookup"><span data-stu-id="ccf20-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="ccf20-119">이 명령은 IpRule 개체를 사용 하 여 여러 IpRule를 추가 하 고 JSON으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="ccf20-120">변수</span><span class="sxs-lookup"><span data-stu-id="ccf20-120">PARAMETERS</span></span>

### <span data-ttu-id="ccf20-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccf20-121">-AsJob</span></span>
<span data-ttu-id="ccf20-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ccf20-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccf20-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf20-123">-DefaultProfile</span></span>
<span data-ttu-id="ccf20-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf20-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ccf20-125">-IPAddressOrRange</span></span>
<span data-ttu-id="ccf20-126">IpAddressOrRange의 배열, 입력 IpAddressOrRange 및 기본 동작을 사용 하 여 IpRules를 추가 합니다. 네트워크 규칙 속성을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="ccf20-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ccf20-127">-IPRule</span></span>
<span data-ttu-id="ccf20-128">NetworkRule 속성에 추가할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="ccf20-129">-이름</span><span class="sxs-lookup"><span data-stu-id="ccf20-129">-Name</span></span>
<span data-ttu-id="ccf20-130">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ccf20-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf20-131">-ResourceGroupName</span></span>
<span data-ttu-id="ccf20-132">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ccf20-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ccf20-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ccf20-134">VirtualNetworkResourceId의 배열은 입력 VirtualNetworkResourceId를 사용 하 여 VirtualNetworkRule를 추가 하 고 네트워크 규칙 속성을 허용 하는 기본 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="ccf20-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ccf20-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="ccf20-136">NetworkRule 속성에 추가할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="ccf20-137">-확인</span><span class="sxs-lookup"><span data-stu-id="ccf20-137">-Confirm</span></span>
<span data-ttu-id="ccf20-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf20-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf20-139">-WhatIf</span></span>
<span data-ttu-id="ccf20-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf20-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf20-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf20-142">CommonParameters</span></span>
<span data-ttu-id="ccf20-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf20-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf20-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf20-145">입력</span><span class="sxs-lookup"><span data-stu-id="ccf20-145">INPUTS</span></span>

### <span data-ttu-id="ccf20-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ccf20-146">System.String</span></span>

### <span data-ttu-id="ccf20-147">PSIpRule []를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ccf20-148">PSVirtualNetworkRule []를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ccf20-149">출력</span><span class="sxs-lookup"><span data-stu-id="ccf20-149">OUTPUTS</span></span>

### <span data-ttu-id="ccf20-150">PSVirtualNetworkRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="ccf20-151">PSIpRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf20-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="ccf20-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ccf20-152">NOTES</span></span>

## <span data-ttu-id="ccf20-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccf20-153">RELATED LINKS</span></span>
