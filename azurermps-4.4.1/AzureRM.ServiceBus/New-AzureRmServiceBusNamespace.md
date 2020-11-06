---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535431"
---
# <span data-ttu-id="0b2c9-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="0b2c9-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="0b2c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2c9-103">새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b2c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b2c9-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b2c9-105">DESCRIPTION</span></span>
<span data-ttu-id="0b2c9-106">**새 AzureRmServiceBusNamespace** cmdlet은 새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="0b2c9-107">네임 스페이스 리소스 매니페스트를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="0b2c9-108">이 작업은 idempotent입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-108">This operation is idempotent.</span></span>

## <span data-ttu-id="0b2c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0b2c9-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2c9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b2c9-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="0b2c9-111">지정 된 리소스 그룹 내에 새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="0b2c9-112">변수</span><span class="sxs-lookup"><span data-stu-id="0b2c9-112">PARAMETERS</span></span>

### <span data-ttu-id="0b2c9-113">-위치</span><span class="sxs-lookup"><span data-stu-id="0b2c9-113">-Location</span></span>
<span data-ttu-id="0b2c9-114">Service Bus 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="0b2c9-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0b2c9-115">-NamespaceName</span></span>
<span data-ttu-id="0b2c9-116">Service Bus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="0b2c9-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-118">The resource group name.</span></span>

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

### <span data-ttu-id="0b2c9-119">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="0b2c9-119">-SkuName</span></span>
<span data-ttu-id="0b2c9-120">Service Bus 네임 스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-120">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="0b2c9-121">태그</span><span class="sxs-lookup"><span data-stu-id="0b2c9-121">-Tag</span></span>
<span data-ttu-id="0b2c9-122">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="0b2c9-123">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="0b2c9-123">For example:</span></span>

<span data-ttu-id="0b2c9-124">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0b2c9-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0b2c9-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0b2c9-125">-Confirm</span></span>
<span data-ttu-id="0b2c9-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2c9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2c9-127">-WhatIf</span></span>
<span data-ttu-id="0b2c9-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b2c9-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2c9-130">CommonParameters</span></span>
<span data-ttu-id="0b2c9-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2c9-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2c9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2c9-133">입력</span><span class="sxs-lookup"><span data-stu-id="0b2c9-133">INPUTS</span></span>

### <span data-ttu-id="0b2c9-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b2c9-134">-ResourceGroup</span></span>
 <span data-ttu-id="0b2c9-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b2c9-135">System.String</span></span>

### <span data-ttu-id="0b2c9-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0b2c9-136">-NamespaceName</span></span>
 <span data-ttu-id="0b2c9-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b2c9-137">System.String</span></span>

### <span data-ttu-id="0b2c9-138">-위치</span><span class="sxs-lookup"><span data-stu-id="0b2c9-138">-Location</span></span>
 <span data-ttu-id="0b2c9-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b2c9-139">System.String</span></span>

### <span data-ttu-id="0b2c9-140">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="0b2c9-140">-SkuName</span></span>
 <span data-ttu-id="0b2c9-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b2c9-141">System.String</span></span>

### <span data-ttu-id="0b2c9-142">태그</span><span class="sxs-lookup"><span data-stu-id="0b2c9-142">-Tag</span></span>
 <span data-ttu-id="0b2c9-143">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0b2c9-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b2c9-144">출력</span><span class="sxs-lookup"><span data-stu-id="0b2c9-144">OUTPUTS</span></span>

### <span data-ttu-id="0b2c9-145">ServiceBus. NamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="0b2c9-146">상속자</span><span class="sxs-lookup"><span data-stu-id="0b2c9-146">NOTES</span></span>

## <span data-ttu-id="0b2c9-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b2c9-147">RELATED LINKS</span></span>
