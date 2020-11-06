---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531653"
---
# <span data-ttu-id="1b8b4-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1b8b4-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="1b8b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8b4-103">새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b8b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b8b4-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b8b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1b8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="1b8b4-106">**새 AzureRmServiceBusNamespace** cmdlet은 새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="1b8b4-107">네임 스페이스 리소스 매니페스트를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="1b8b4-108">이 작업은 idempotent입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-108">This operation is idempotent.</span></span>

## <span data-ttu-id="1b8b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1b8b4-109">EXAMPLES</span></span>

### <span data-ttu-id="1b8b4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b8b4-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="1b8b4-111">지정 된 리소스 그룹 내에 새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="1b8b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="1b8b4-112">PARAMETERS</span></span>

### <span data-ttu-id="1b8b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b8b4-113">-DefaultProfile</span></span>
<span data-ttu-id="1b8b4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b8b4-115">-위치</span><span class="sxs-lookup"><span data-stu-id="1b8b4-115">-Location</span></span>
<span data-ttu-id="1b8b4-116">Service Bus 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="1b8b4-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1b8b4-117">-Name</span></span>
<span data-ttu-id="1b8b4-118">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="1b8b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b8b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b8b4-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-120">The resource group name.</span></span>

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

### <span data-ttu-id="1b8b4-121">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="1b8b4-121">-SkuName</span></span>
<span data-ttu-id="1b8b4-122">Service Bus 네임 스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="1b8b4-123">태그</span><span class="sxs-lookup"><span data-stu-id="1b8b4-123">-Tag</span></span>
<span data-ttu-id="1b8b4-124">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="1b8b4-125">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="1b8b4-125">For example:</span></span>

<span data-ttu-id="1b8b4-126">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1b8b4-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1b8b4-127">-확인</span><span class="sxs-lookup"><span data-stu-id="1b8b4-127">-Confirm</span></span>
<span data-ttu-id="1b8b4-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b8b4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b8b4-129">-WhatIf</span></span>
<span data-ttu-id="1b8b4-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b8b4-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b8b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8b4-132">CommonParameters</span></span>
<span data-ttu-id="1b8b4-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b8b4-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b8b4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8b4-135">입력</span><span class="sxs-lookup"><span data-stu-id="1b8b4-135">INPUTS</span></span>

### <span data-ttu-id="1b8b4-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1b8b4-136">-ResourceGroup</span></span>
 <span data-ttu-id="1b8b4-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1b8b4-137">System.String</span></span>

### <span data-ttu-id="1b8b4-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1b8b4-138">-NamespaceName</span></span>
 <span data-ttu-id="1b8b4-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1b8b4-139">System.String</span></span>

### <span data-ttu-id="1b8b4-140">-위치</span><span class="sxs-lookup"><span data-stu-id="1b8b4-140">-Location</span></span>
 <span data-ttu-id="1b8b4-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1b8b4-141">System.String</span></span>

### <span data-ttu-id="1b8b4-142">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="1b8b4-142">-SkuName</span></span>
 <span data-ttu-id="1b8b4-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1b8b4-143">System.String</span></span>

### <span data-ttu-id="1b8b4-144">태그</span><span class="sxs-lookup"><span data-stu-id="1b8b4-144">-Tag</span></span>
 <span data-ttu-id="1b8b4-145">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1b8b4-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b8b4-146">출력</span><span class="sxs-lookup"><span data-stu-id="1b8b4-146">OUTPUTS</span></span>

### <span data-ttu-id="1b8b4-147">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="1b8b4-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1b8b4-148">상속자</span><span class="sxs-lookup"><span data-stu-id="1b8b4-148">NOTES</span></span>

## <span data-ttu-id="1b8b4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b8b4-149">RELATED LINKS</span></span>

