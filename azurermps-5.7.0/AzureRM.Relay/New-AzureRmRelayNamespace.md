---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531677"
---
# <span data-ttu-id="012a0-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="012a0-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="012a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="012a0-102">SYNOPSIS</span></span>
<span data-ttu-id="012a0-103">새 릴레이 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="012a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="012a0-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="012a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="012a0-105">DESCRIPTION</span></span>
<span data-ttu-id="012a0-106">새 릴레이 네임 스페이스를 만드는 **AzureRmRelayNamespace** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="012a0-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="012a0-107">네임 스페이스 리소스 매니페스트를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="012a0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="012a0-108">EXAMPLES</span></span>

### <span data-ttu-id="012a0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="012a0-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="012a0-110">지정 된 리소스 그룹 내에 새 릴레이 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="012a0-111">변수</span><span class="sxs-lookup"><span data-stu-id="012a0-111">PARAMETERS</span></span>

### <span data-ttu-id="012a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012a0-112">-DefaultProfile</span></span>
<span data-ttu-id="012a0-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="012a0-114">-위치</span><span class="sxs-lookup"><span data-stu-id="012a0-114">-Location</span></span>
<span data-ttu-id="012a0-115">릴레이 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="012a0-116">-이름</span><span class="sxs-lookup"><span data-stu-id="012a0-116">-Name</span></span>
<span data-ttu-id="012a0-117">릴레이 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="012a0-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="012a0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="012a0-118">-ResourceGroupName</span></span>
<span data-ttu-id="012a0-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="012a0-120">태그</span><span class="sxs-lookup"><span data-stu-id="012a0-120">-Tag</span></span>
<span data-ttu-id="012a0-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="012a0-122">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="012a0-122">For example:</span></span>

<span data-ttu-id="012a0-123">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="012a0-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="012a0-124">-확인</span><span class="sxs-lookup"><span data-stu-id="012a0-124">-Confirm</span></span>
<span data-ttu-id="012a0-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="012a0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="012a0-126">-WhatIf</span></span>
<span data-ttu-id="012a0-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="012a0-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="012a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012a0-129">CommonParameters</span></span>
<span data-ttu-id="012a0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="012a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012a0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="012a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012a0-132">입력</span><span class="sxs-lookup"><span data-stu-id="012a0-132">INPUTS</span></span>

### <span data-ttu-id="012a0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="012a0-133">-ResourceGroupName</span></span>
 <span data-ttu-id="012a0-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="012a0-134">System.String</span></span>

### <span data-ttu-id="012a0-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="012a0-135">-NamespaceName</span></span>
 <span data-ttu-id="012a0-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="012a0-136">System.String</span></span>

### <span data-ttu-id="012a0-137">-위치</span><span class="sxs-lookup"><span data-stu-id="012a0-137">-Location</span></span>
 <span data-ttu-id="012a0-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="012a0-138">System.String</span></span>

### <span data-ttu-id="012a0-139">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="012a0-139">-SkuName</span></span>
 <span data-ttu-id="012a0-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="012a0-140">System.String</span></span>

### <span data-ttu-id="012a0-141">태그</span><span class="sxs-lookup"><span data-stu-id="012a0-141">-Tag</span></span>
 <span data-ttu-id="012a0-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="012a0-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="012a0-143">출력</span><span class="sxs-lookup"><span data-stu-id="012a0-143">OUTPUTS</span></span>

### <span data-ttu-id="012a0-144">RelayNamespaceAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="012a0-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="012a0-145">상속자</span><span class="sxs-lookup"><span data-stu-id="012a0-145">NOTES</span></span>

## <span data-ttu-id="012a0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="012a0-146">RELATED LINKS</span></span>

