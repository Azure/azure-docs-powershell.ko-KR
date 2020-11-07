---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704201"
---
# <span data-ttu-id="0c370-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c370-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="0c370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c370-102">SYNOPSIS</span></span>
<span data-ttu-id="0c370-103">저장소 계정의 NetworkRule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="0c370-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c370-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c370-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c370-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c370-105">DESCRIPTION</span></span>
<span data-ttu-id="0c370-106">**업데이트-AzureRmStorageAccountNetworkRuleSet** Cmdlet이 저장소 계정의 networkrule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="0c370-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="0c370-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0c370-107">EXAMPLES</span></span>

### <span data-ttu-id="0c370-108">예제 1: NetworkRule의 모든 속성 업데이트, JSON을 사용 하 여 입력 규칙</span><span class="sxs-lookup"><span data-stu-id="0c370-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="0c370-109">이 명령은 모든 NetworkRule의 속성, JSON으로 입력 하는 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="0c370-110">예제 2: NetworkRule의 업데이트 무시 속성</span><span class="sxs-lookup"><span data-stu-id="0c370-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="0c370-111">이 명령은 NetworkRule의 Bypass 속성을 업데이트 합니다 (다른 속성은 변경 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="0c370-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="0c370-112">예제 3: 저장소 계정의 NetworkRule 규칙 정리</span><span class="sxs-lookup"><span data-stu-id="0c370-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="0c370-113">이 명령은 저장소 계정의 NetworkRule 규칙을 정리 합니다 (다른 속성은 변경 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="0c370-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="0c370-114">변수</span><span class="sxs-lookup"><span data-stu-id="0c370-114">PARAMETERS</span></span>

### <span data-ttu-id="0c370-115">-바이패스</span><span class="sxs-lookup"><span data-stu-id="0c370-115">-Bypass</span></span>
<span data-ttu-id="0c370-116">저장소 계정의 NetworkRule 속성으로 업데이트할 우회 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="0c370-117">허용 되는 값은 없음 또는 다음의 조합입니다. a € i n i i 로깅 서비스</span><span class="sxs-lookup"><span data-stu-id="0c370-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

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

### <span data-ttu-id="0c370-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="0c370-118">-DefaultAction</span></span>
<span data-ttu-id="0c370-119">저장소 계정의 NetworkRule 속성으로 업데이트할 DefaultAction 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="0c370-120">허용 되는 옵션: a € 거부 허용</span><span class="sxs-lookup"><span data-stu-id="0c370-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c370-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="0c370-121">-IPRule</span></span>
<span data-ttu-id="0c370-122">저장소 계정의 NetworkRule 속성으로 업데이트할 IpRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="0c370-123">-이름</span><span class="sxs-lookup"><span data-stu-id="0c370-123">-Name</span></span>
<span data-ttu-id="0c370-124">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-124">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="0c370-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c370-125">-ResourceGroupName</span></span>
<span data-ttu-id="0c370-126">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="0c370-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0c370-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="0c370-128">저장소 계정의 NetworkRule 속성으로 업데이트할 VirtualNetworkRule 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="0c370-129">-확인</span><span class="sxs-lookup"><span data-stu-id="0c370-129">-Confirm</span></span>
<span data-ttu-id="0c370-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c370-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c370-131">-WhatIf</span></span>
<span data-ttu-id="0c370-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c370-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c370-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c370-134">-DefaultProfile</span></span>
<span data-ttu-id="0c370-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c370-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c370-136">CommonParameters</span></span>
<span data-ttu-id="0c370-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c370-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c370-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c370-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c370-139">입력</span><span class="sxs-lookup"><span data-stu-id="0c370-139">INPUTS</span></span>

### <span data-ttu-id="0c370-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c370-140">System.String</span></span>
<span data-ttu-id="0c370-141">PSIpRule []. PSVirtualNetworkRule [].. \* ". \* \*. \* \*.</span><span class="sxs-lookup"><span data-stu-id="0c370-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="0c370-142">출력</span><span class="sxs-lookup"><span data-stu-id="0c370-142">OUTPUTS</span></span>

### <span data-ttu-id="0c370-143">Microsoft Azure.. m a. 모델. PSNetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="0c370-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="0c370-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0c370-144">NOTES</span></span>

## <span data-ttu-id="0c370-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c370-145">RELATED LINKS</span></span>

