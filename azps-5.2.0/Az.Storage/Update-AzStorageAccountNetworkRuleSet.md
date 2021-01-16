---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367494"
---
# <span data-ttu-id="adc91-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="adc91-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="adc91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc91-102">SYNOPSIS</span></span>
<span data-ttu-id="adc91-103">Storage 계정의 NetworkRule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="adc91-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="adc91-104">구문</span><span class="sxs-lookup"><span data-stu-id="adc91-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc91-105">설명</span><span class="sxs-lookup"><span data-stu-id="adc91-105">DESCRIPTION</span></span>
<span data-ttu-id="adc91-106">**Update-AzStorageAccountNetworkRuleSet** cmdlet은 Storage 계정의 NetworkRule 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="adc91-107">예제</span><span class="sxs-lookup"><span data-stu-id="adc91-107">EXAMPLES</span></span>

### <span data-ttu-id="adc91-108">예제 1: NetworkRule의 모든 속성 업데이트, JSON을 사용하여 입력 규칙</span><span class="sxs-lookup"><span data-stu-id="adc91-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="adc91-109">이 명령은 NetworkRule의 모든 속성을 업데이트하고 JSON을 사용하여 규칙을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="adc91-110">예제 2: NetworkRule의 우회 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="adc91-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="adc91-111">이 명령은 NetworkRule의 우회 속성을 업데이트합니다(다른 속성은 변경되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="adc91-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="adc91-112">예제 3: Storage 계정의 NetworkRule 규칙 정리</span><span class="sxs-lookup"><span data-stu-id="adc91-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="adc91-113">이 명령은 Storage 계정의 NetworkRule 규칙을 정리합니다(다른 속성은 변경되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="adc91-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="adc91-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adc91-114">PARAMETERS</span></span>

### <span data-ttu-id="adc91-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adc91-115">-AsJob</span></span>
<span data-ttu-id="adc91-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="adc91-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adc91-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="adc91-117">-Bypass</span></span>
<span data-ttu-id="adc91-118">Storage 계정의 NetworkRule 속성으로 업데이트할 우회 값입니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="adc91-119">허용되는 값은 없음 또는 임의 조합입니다. • 로깅 • 메트릭 • Azure 서비스</span><span class="sxs-lookup"><span data-stu-id="adc91-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc91-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="adc91-120">-DefaultAction</span></span>
<span data-ttu-id="adc91-121">Storage 계정의 NetworkRule 속성으로 업데이트할 DefaultAction 값입니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="adc91-122">허용되는 옵션: • 허용 • 거부</span><span class="sxs-lookup"><span data-stu-id="adc91-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc91-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc91-123">-DefaultProfile</span></span>
<span data-ttu-id="adc91-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc91-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="adc91-125">-IPRule</span></span>
<span data-ttu-id="adc91-126">Storage 계정의 NetworkRule 속성으로 업데이트할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adc91-127">-Name</span><span class="sxs-lookup"><span data-stu-id="adc91-127">-Name</span></span>
<span data-ttu-id="adc91-128">Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="adc91-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc91-129">-ResourceGroupName</span></span>
<span data-ttu-id="adc91-130">Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="adc91-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="adc91-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="adc91-132">Storage 계정의 NetworkRule 속성으로 업데이트할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adc91-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adc91-133">-Confirm</span></span>
<span data-ttu-id="adc91-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc91-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc91-135">-WhatIf</span></span>
<span data-ttu-id="adc91-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="adc91-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc91-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc91-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc91-138">CommonParameters</span></span>
<span data-ttu-id="adc91-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="adc91-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc91-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="adc91-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc91-141">입력</span><span class="sxs-lookup"><span data-stu-id="adc91-141">INPUTS</span></span>

### <span data-ttu-id="adc91-142">System.String</span><span class="sxs-lookup"><span data-stu-id="adc91-142">System.String</span></span>

### <span data-ttu-id="adc91-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="adc91-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="adc91-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="adc91-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="adc91-145">출력</span><span class="sxs-lookup"><span data-stu-id="adc91-145">OUTPUTS</span></span>

### <span data-ttu-id="adc91-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="adc91-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="adc91-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="adc91-147">NOTES</span></span>

## <span data-ttu-id="adc91-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc91-148">RELATED LINKS</span></span>
