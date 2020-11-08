---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044308"
---
# <span data-ttu-id="a658b-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a658b-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="a658b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a658b-102">SYNOPSIS</span></span>
<span data-ttu-id="a658b-103">기존 Service Bus 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="a658b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a658b-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a658b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a658b-105">DESCRIPTION</span></span>
<span data-ttu-id="a658b-106">**AzServiceBusNamespace** cmdlet은 리소스 그룹 내의 지정 된 Service Bus 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="a658b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a658b-107">EXAMPLES</span></span>

### <span data-ttu-id="a658b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a658b-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="a658b-109">새 설명으로 Service Bus 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="a658b-110">변수</span><span class="sxs-lookup"><span data-stu-id="a658b-110">PARAMETERS</span></span>

### <span data-ttu-id="a658b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a658b-111">-DefaultProfile</span></span>
<span data-ttu-id="a658b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a658b-113">-위치</span><span class="sxs-lookup"><span data-stu-id="a658b-113">-Location</span></span>
<span data-ttu-id="a658b-114">Service Bus 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-114">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a658b-115">-Name</span></span>
<span data-ttu-id="a658b-116">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a658b-117">-ResourceGroupName</span></span>
<span data-ttu-id="a658b-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a658b-119">-SkuCapacity</span></span>
<span data-ttu-id="a658b-120">네임 스페이스 Sku 용량.</span><span class="sxs-lookup"><span data-stu-id="a658b-120">Namespace Sku Capacity.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-121">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="a658b-121">-SkuName</span></span>
<span data-ttu-id="a658b-122">네임 스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-122">The namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-123">태그</span><span class="sxs-lookup"><span data-stu-id="a658b-123">-Tag</span></span>
<span data-ttu-id="a658b-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a658b-125">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a658b-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-126">-확인</span><span class="sxs-lookup"><span data-stu-id="a658b-126">-Confirm</span></span>
<span data-ttu-id="a658b-127">지정 된 정보로 Service Bus 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-127">Updates the Service Bus namespace with the specified information.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a658b-128">-WhatIf</span></span>
<span data-ttu-id="a658b-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a658b-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a658b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a658b-131">CommonParameters</span></span>
<span data-ttu-id="a658b-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a658b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a658b-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a658b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a658b-134">입력</span><span class="sxs-lookup"><span data-stu-id="a658b-134">INPUTS</span></span>

### <span data-ttu-id="a658b-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a658b-135">System.String</span></span>

### <span data-ttu-id="a658b-136">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="a658b-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a658b-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a658b-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a658b-138">출력</span><span class="sxs-lookup"><span data-stu-id="a658b-138">OUTPUTS</span></span>

### <span data-ttu-id="a658b-139">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="a658b-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a658b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="a658b-140">NOTES</span></span>

## <span data-ttu-id="a658b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a658b-141">RELATED LINKS</span></span>
