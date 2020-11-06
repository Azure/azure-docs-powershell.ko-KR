---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: f4a94823ba0ff615a68a9e17703ba7e8193b0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531638"
---
# <span data-ttu-id="ea155-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ea155-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="ea155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea155-102">SYNOPSIS</span></span>
<span data-ttu-id="ea155-103">기존 Service Bus 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea155-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea155-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea155-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea155-105">DESCRIPTION</span></span>
<span data-ttu-id="ea155-106">**AzureRmServiceBusNamespace** cmdlet은 리소스 그룹 내의 지정 된 Service Bus 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="ea155-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ea155-107">EXAMPLES</span></span>

### <span data-ttu-id="ea155-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea155-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="ea155-109">새 설명으로 Service Bus 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="ea155-110">변수</span><span class="sxs-lookup"><span data-stu-id="ea155-110">PARAMETERS</span></span>

### <span data-ttu-id="ea155-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea155-111">-DefaultProfile</span></span>
<span data-ttu-id="ea155-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea155-113">-위치</span><span class="sxs-lookup"><span data-stu-id="ea155-113">-Location</span></span>
<span data-ttu-id="ea155-114">Service Bus 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-114">The Service Bus namespace location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ea155-115">-Name</span></span>
<span data-ttu-id="ea155-116">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea155-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea155-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ea155-119">-SkuCapacity</span></span>
<span data-ttu-id="ea155-120">네임 스페이스 Sku 용량.</span><span class="sxs-lookup"><span data-stu-id="ea155-120">Namespace Sku Capacity.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-121">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="ea155-121">-SkuName</span></span>
<span data-ttu-id="ea155-122">네임 스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-122">The namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-123">태그</span><span class="sxs-lookup"><span data-stu-id="ea155-123">-Tag</span></span>
<span data-ttu-id="ea155-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea155-125">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ea155-125">For example:</span></span>

<span data-ttu-id="ea155-126">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ea155-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-127">-확인</span><span class="sxs-lookup"><span data-stu-id="ea155-127">-Confirm</span></span>
<span data-ttu-id="ea155-128">지정 된 정보로 Service Bus 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-128">Updates the Service Bus namespace with the specified information.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea155-129">-WhatIf</span></span>
<span data-ttu-id="ea155-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea155-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea155-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea155-132">CommonParameters</span></span>
<span data-ttu-id="ea155-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea155-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea155-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea155-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea155-135">입력</span><span class="sxs-lookup"><span data-stu-id="ea155-135">INPUTS</span></span>

### <span data-ttu-id="ea155-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea155-136">-ResourceGroup</span></span>
 <span data-ttu-id="ea155-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea155-137">System.String</span></span>

### <span data-ttu-id="ea155-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ea155-138">-NamespaceName</span></span>
 <span data-ttu-id="ea155-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea155-139">System.String</span></span>

### <span data-ttu-id="ea155-140">-위치</span><span class="sxs-lookup"><span data-stu-id="ea155-140">-Location</span></span>
 <span data-ttu-id="ea155-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea155-141">System.String</span></span>

### <span data-ttu-id="ea155-142">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="ea155-142">-SkuName</span></span>
 <span data-ttu-id="ea155-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea155-143">System.String</span></span>

### <span data-ttu-id="ea155-144">태그</span><span class="sxs-lookup"><span data-stu-id="ea155-144">-Tag</span></span>
 <span data-ttu-id="ea155-145">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ea155-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ea155-146">출력</span><span class="sxs-lookup"><span data-stu-id="ea155-146">OUTPUTS</span></span>

### <span data-ttu-id="ea155-147">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="ea155-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ea155-148">상속자</span><span class="sxs-lookup"><span data-stu-id="ea155-148">NOTES</span></span>


## <span data-ttu-id="ea155-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea155-149">RELATED LINKS</span></span>

