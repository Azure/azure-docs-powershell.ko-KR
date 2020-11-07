---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711490"
---
# <span data-ttu-id="64053-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="64053-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="64053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64053-102">SYNOPSIS</span></span>
<span data-ttu-id="64053-103">Service Bus 큐에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64053-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64053-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64053-105">설명은</span><span class="sxs-lookup"><span data-stu-id="64053-105">DESCRIPTION</span></span>
<span data-ttu-id="64053-106">**AzureRmServiceBusQueueKey** cmdlet은 지정 된 Service Bus 큐 및 권한 부여 규칙에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="64053-107">예제의</span><span class="sxs-lookup"><span data-stu-id="64053-107">EXAMPLES</span></span>

### <span data-ttu-id="64053-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="64053-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="64053-109">네임 스페이스에 대 한 기본 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="64053-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="64053-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="64053-111">네임 스페이스에 대 한 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="64053-112">변수</span><span class="sxs-lookup"><span data-stu-id="64053-112">PARAMETERS</span></span>

### <span data-ttu-id="64053-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="64053-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="64053-114">인증 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64053-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64053-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="64053-115">-NamespaceName</span></span>
<span data-ttu-id="64053-116">Service Bus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64053-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="64053-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="64053-117">-QueueName</span></span>
<span data-ttu-id="64053-118">Service Bus 큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64053-118">The Service Bus queue name.</span></span>

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

### <span data-ttu-id="64053-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="64053-119">-RegenerateKeys</span></span>
<span data-ttu-id="64053-120">기본 또는 보조 키를 다시 생성할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64053-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64053-121">-ResourceGroup</span></span>
<span data-ttu-id="64053-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64053-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="64053-123">-확인</span><span class="sxs-lookup"><span data-stu-id="64053-123">-Confirm</span></span>
<span data-ttu-id="64053-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64053-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64053-125">-WhatIf</span></span>
<span data-ttu-id="64053-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64053-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64053-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64053-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64053-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64053-128">CommonParameters</span></span>
<span data-ttu-id="64053-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64053-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64053-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64053-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64053-131">입력</span><span class="sxs-lookup"><span data-stu-id="64053-131">INPUTS</span></span>

### <span data-ttu-id="64053-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64053-132">-ResourceGroup</span></span>
 <span data-ttu-id="64053-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64053-133">System.String</span></span>
 

### <span data-ttu-id="64053-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="64053-134">-NamespaceName</span></span>
 <span data-ttu-id="64053-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64053-135">System.String</span></span>
 

### <span data-ttu-id="64053-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="64053-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="64053-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64053-137">System.String</span></span>
 

### <span data-ttu-id="64053-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="64053-138">-QueueName</span></span>
 <span data-ttu-id="64053-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64053-139">System.String</span></span>
 

### <span data-ttu-id="64053-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="64053-140">-RegenerateKeys</span></span>
 <span data-ttu-id="64053-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64053-141">System.String</span></span>

## <span data-ttu-id="64053-142">출력</span><span class="sxs-lookup"><span data-stu-id="64053-142">OUTPUTS</span></span>

### <span data-ttu-id="64053-143">ServiceBus-. m m g 목록 키</span><span class="sxs-lookup"><span data-stu-id="64053-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="64053-144">PrimaryConnectionString: 끝점 = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-Queue_exa mpl1 PrimaryKey: {PrimaryKey 값} SecondaryKey: {SecondaryKey 값} KeyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="64053-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="64053-145">상속자</span><span class="sxs-lookup"><span data-stu-id="64053-145">NOTES</span></span>

## <span data-ttu-id="64053-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64053-146">RELATED LINKS</span></span>

