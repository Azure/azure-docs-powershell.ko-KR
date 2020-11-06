---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: b6ec1908af93642cf064b72b1a78a64641749409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526527"
---
# <span data-ttu-id="997da-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="997da-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="997da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="997da-102">SYNOPSIS</span></span>
 <span data-ttu-id="997da-103">저장소 계정의 네트워크 규칙 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="997da-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="997da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="997da-104">SYNTAX</span></span>

### <span data-ttu-id="997da-105">NetWorkRuleString (기본값)</span><span class="sxs-lookup"><span data-stu-id="997da-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="997da-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="997da-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="997da-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="997da-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="997da-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="997da-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="997da-109">설명은</span><span class="sxs-lookup"><span data-stu-id="997da-109">DESCRIPTION</span></span>
<span data-ttu-id="997da-110">**추가-AzureRmStorageAccountNetworkRule** Cmdlet은 저장소 계정의 networkrule 속성에 IpRules 또는 VirtualNetworkRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="997da-111">예제의</span><span class="sxs-lookup"><span data-stu-id="997da-111">EXAMPLES</span></span>

### <span data-ttu-id="997da-112">예제 1: IPAddressOrRange를 사용 하 여 여러 IpRules 추가</span><span class="sxs-lookup"><span data-stu-id="997da-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="997da-113">이 명령은 IPAddressOrRange로 여러 IpRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="997da-114">예제 2: VirtualNetworkResourceID를 사용 하 여 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="997da-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="997da-115">이 명령은 VirtualNetworkResourceID를 사용 하 여 VirtualNetworkRule를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="997da-116">예제 3: 다른 계정의 VirtualNetworkRule 개체를 사용 하 여 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="997da-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="997da-117">이 명령은 다른 계정의 VirtualNetworkRule 개체를 사용 하 여 VirtualNetworkRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="997da-118">예제 4: IpRule 개체를 사용 하 여 여러 IpRule 추가, JSON으로 입력</span><span class="sxs-lookup"><span data-stu-id="997da-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="997da-119">이 명령은 IpRule 개체를 사용 하 여 여러 IpRule를 추가 하 고 JSON으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="997da-120">변수</span><span class="sxs-lookup"><span data-stu-id="997da-120">PARAMETERS</span></span>

### <span data-ttu-id="997da-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="997da-121">-AsJob</span></span>
<span data-ttu-id="997da-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="997da-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="997da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="997da-123">-DefaultProfile</span></span>
<span data-ttu-id="997da-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="997da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997da-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="997da-125">-IPAddressOrRange</span></span>
<span data-ttu-id="997da-126">IpAddressOrRange의 배열, 입력 IpAddressOrRange 및 기본 동작을 사용 하 여 IpRules를 추가 합니다. 네트워크 규칙 속성을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: IpRuleString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997da-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="997da-127">-IPRule</span></span>
<span data-ttu-id="997da-128">NetworkRule 속성에 추가할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="997da-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: IpRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="997da-129">-이름</span><span class="sxs-lookup"><span data-stu-id="997da-129">-Name</span></span>
<span data-ttu-id="997da-130">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="997da-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="997da-131">-ResourceGroupName</span></span>
<span data-ttu-id="997da-132">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="997da-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="997da-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="997da-134">VirtualNetworkResourceId의 배열은 입력 VirtualNetworkResourceId를 사용 하 여 VirtualNetworkRule를 추가 하 고 네트워크 규칙 속성을 허용 하는 기본 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997da-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="997da-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="997da-136">NetworkRule 속성에 추가할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="997da-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="997da-137">-확인</span><span class="sxs-lookup"><span data-stu-id="997da-137">-Confirm</span></span>
<span data-ttu-id="997da-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="997da-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="997da-139">-WhatIf</span></span>
<span data-ttu-id="997da-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="997da-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="997da-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="997da-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="997da-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="997da-142">CommonParameters</span></span>
<span data-ttu-id="997da-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="997da-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="997da-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="997da-145">입력</span><span class="sxs-lookup"><span data-stu-id="997da-145">INPUTS</span></span>

### <span data-ttu-id="997da-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="997da-146">System.String</span></span>
<span data-ttu-id="997da-147">PSIpRule []. PSVirtualNetworkRule [].. \* ". \* \*. \* \*.</span><span class="sxs-lookup"><span data-stu-id="997da-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="997da-148">출력</span><span class="sxs-lookup"><span data-stu-id="997da-148">OUTPUTS</span></span>

### <span data-ttu-id="997da-149">PSVirtualNetworkRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="997da-150">PSIpRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="997da-150">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="997da-151">상속자</span><span class="sxs-lookup"><span data-stu-id="997da-151">NOTES</span></span>

## <span data-ttu-id="997da-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="997da-152">RELATED LINKS</span></span>

