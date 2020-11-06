---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 8851f7e2820e1c9a0a63b475544c49fe5c0c8ee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533555"
---
# <span data-ttu-id="f80d3-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f80d3-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f80d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f80d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f80d3-103">저장소 계정의 NetworkRule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f80d3-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f80d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f80d3-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f80d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f80d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f80d3-106">**업데이트-AzureRmStorageAccountNetworkRuleSet** Cmdlet이 저장소 계정의 networkrule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f80d3-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f80d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f80d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f80d3-108">예제 1: NetworkRule의 모든 속성 업데이트, JSON을 사용 하 여 입력 규칙</span><span class="sxs-lookup"><span data-stu-id="f80d3-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="f80d3-109">이 명령은 모든 NetworkRule의 속성, JSON으로 입력 하는 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="f80d3-110">예제 2: NetworkRule의 업데이트 무시 속성</span><span class="sxs-lookup"><span data-stu-id="f80d3-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="f80d3-111">이 명령은 NetworkRule의 Bypass 속성을 업데이트 합니다 (다른 속성은 변경 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="f80d3-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="f80d3-112">예제 3: 저장소 계정의 NetworkRule 규칙 정리</span><span class="sxs-lookup"><span data-stu-id="f80d3-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="f80d3-113">이 명령은 저장소 계정의 NetworkRule 규칙을 정리 합니다 (다른 속성은 변경 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="f80d3-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="f80d3-114">변수</span><span class="sxs-lookup"><span data-stu-id="f80d3-114">PARAMETERS</span></span>

### <span data-ttu-id="f80d3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f80d3-115">-AsJob</span></span>
<span data-ttu-id="f80d3-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f80d3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f80d3-117">-바이패스</span><span class="sxs-lookup"><span data-stu-id="f80d3-117">-Bypass</span></span>
<span data-ttu-id="f80d3-118">저장소 계정의 NetworkRule 속성으로 업데이트할 우회 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="f80d3-119">허용 되는 값은 없음 또는: • Logging • 메트릭스 • Azureservices의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80d3-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="f80d3-120">-DefaultAction</span></span>
<span data-ttu-id="f80d3-121">저장소 계정의 NetworkRule 속성으로 업데이트할 DefaultAction 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="f80d3-122">허용 되는 옵션: • Allow • Deny</span><span class="sxs-lookup"><span data-stu-id="f80d3-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80d3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80d3-123">-DefaultProfile</span></span>
<span data-ttu-id="f80d3-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f80d3-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f80d3-125">-IPRule</span></span>
<span data-ttu-id="f80d3-126">저장소 계정의 NetworkRule 속성으로 업데이트할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f80d3-127">-이름</span><span class="sxs-lookup"><span data-stu-id="f80d3-127">-Name</span></span>
<span data-ttu-id="f80d3-128">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f80d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f80d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="f80d3-130">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f80d3-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f80d3-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="f80d3-132">저장소 계정의 NetworkRule 속성으로 업데이트할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f80d3-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f80d3-133">-Confirm</span></span>
<span data-ttu-id="f80d3-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f80d3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f80d3-135">-WhatIf</span></span>
<span data-ttu-id="f80d3-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f80d3-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f80d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80d3-138">CommonParameters</span></span>
<span data-ttu-id="f80d3-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f80d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80d3-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f80d3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80d3-141">입력</span><span class="sxs-lookup"><span data-stu-id="f80d3-141">INPUTS</span></span>

### <span data-ttu-id="f80d3-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f80d3-142">System.String</span></span>
<span data-ttu-id="f80d3-143">PSIpRule []. PSVirtualNetworkRule [].. \* ". \* \*. \* \*.</span><span class="sxs-lookup"><span data-stu-id="f80d3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f80d3-144">출력</span><span class="sxs-lookup"><span data-stu-id="f80d3-144">OUTPUTS</span></span>

### <span data-ttu-id="f80d3-145">Microsoft Azure.. m a. 모델. PSNetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="f80d3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f80d3-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f80d3-146">NOTES</span></span>

## <span data-ttu-id="f80d3-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f80d3-147">RELATED LINKS</span></span>

