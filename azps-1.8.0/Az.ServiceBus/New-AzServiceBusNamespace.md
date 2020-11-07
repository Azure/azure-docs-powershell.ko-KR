---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 8ca2b63b541bb20e6cbde861fc8c1329410335a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699181"
---
# <span data-ttu-id="9a78e-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9a78e-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="9a78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a78e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a78e-103">새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="9a78e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a78e-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a78e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a78e-105">DESCRIPTION</span></span>
<span data-ttu-id="9a78e-106">**새 AzServiceBusNamespace** cmdlet은 새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="9a78e-107">네임 스페이스 리소스 매니페스트를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="9a78e-108">이 작업은 idempotent입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-108">This operation is idempotent.</span></span>

## <span data-ttu-id="9a78e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9a78e-109">EXAMPLES</span></span>

### <span data-ttu-id="9a78e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a78e-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="9a78e-111">지정 된 리소스 그룹 내에 새 Service Bus 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="9a78e-112">변수</span><span class="sxs-lookup"><span data-stu-id="9a78e-112">PARAMETERS</span></span>

### <span data-ttu-id="9a78e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a78e-113">-DefaultProfile</span></span>
<span data-ttu-id="9a78e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a78e-115">-위치</span><span class="sxs-lookup"><span data-stu-id="9a78e-115">-Location</span></span>
<span data-ttu-id="9a78e-116">Service Bus 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="9a78e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9a78e-117">-Name</span></span>
<span data-ttu-id="9a78e-118">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="9a78e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a78e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9a78e-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-120">The resource group name.</span></span>

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

### <span data-ttu-id="9a78e-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9a78e-121">-SkuCapacity</span></span>
<span data-ttu-id="9a78e-122">Service Bus premium 네임 스페이스 처리 단위, 허용 값 1 또는 2 또는 4</span><span class="sxs-lookup"><span data-stu-id="9a78e-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="9a78e-123">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="9a78e-123">-SkuName</span></span>
<span data-ttu-id="9a78e-124">Service Bus 네임 스페이스 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="9a78e-125">태그</span><span class="sxs-lookup"><span data-stu-id="9a78e-125">-Tag</span></span>
<span data-ttu-id="9a78e-126">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9a78e-127">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9a78e-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9a78e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9a78e-128">-Confirm</span></span>
<span data-ttu-id="9a78e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a78e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a78e-130">-WhatIf</span></span>
<span data-ttu-id="9a78e-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a78e-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a78e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a78e-133">CommonParameters</span></span>
<span data-ttu-id="9a78e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a78e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a78e-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a78e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a78e-136">입력</span><span class="sxs-lookup"><span data-stu-id="9a78e-136">INPUTS</span></span>

### <span data-ttu-id="9a78e-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a78e-137">System.String</span></span>

### <span data-ttu-id="9a78e-138">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="9a78e-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9a78e-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="9a78e-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9a78e-140">출력</span><span class="sxs-lookup"><span data-stu-id="9a78e-140">OUTPUTS</span></span>

### <span data-ttu-id="9a78e-141">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="9a78e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9a78e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9a78e-142">NOTES</span></span>

## <span data-ttu-id="9a78e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a78e-143">RELATED LINKS</span></span>
