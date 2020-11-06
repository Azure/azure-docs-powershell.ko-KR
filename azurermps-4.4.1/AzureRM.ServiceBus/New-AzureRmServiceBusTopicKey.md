---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529149"
---
# <span data-ttu-id="966c7-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="966c7-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="966c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="966c7-102">SYNOPSIS</span></span>
<span data-ttu-id="966c7-103">Service Bus 주제에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="966c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="966c7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="966c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="966c7-105">DESCRIPTION</span></span>
<span data-ttu-id="966c7-106">**AzureRmServiceBusTopicKey** cmdlet은 지정 된 Service Bus 항목 및 권한 부여 규칙에 대 한 새 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="966c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="966c7-107">EXAMPLES</span></span>

### <span data-ttu-id="966c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="966c7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="966c7-109">네임 스페이스에 대 한 기본 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="966c7-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="966c7-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="966c7-111">네임 스페이스에 대 한 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="966c7-112">변수</span><span class="sxs-lookup"><span data-stu-id="966c7-112">PARAMETERS</span></span>

### <span data-ttu-id="966c7-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="966c7-113">-RegenerateKeys</span></span>
<span data-ttu-id="966c7-114">기본 또는 보조 키를 다시 생성할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="966c7-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="966c7-115">-ResourceGroup</span></span>
<span data-ttu-id="966c7-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="966c7-117">-확인</span><span class="sxs-lookup"><span data-stu-id="966c7-117">-Confirm</span></span>
<span data-ttu-id="966c7-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="966c7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966c7-119">-WhatIf</span></span>
<span data-ttu-id="966c7-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="966c7-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="966c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966c7-122">-DefaultProfile</span></span>
<span data-ttu-id="966c7-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966c7-124">-이름</span><span class="sxs-lookup"><span data-stu-id="966c7-124">-Name</span></span>
<span data-ttu-id="966c7-125">권한 부여 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966c7-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="966c7-126">-Namespace</span></span>
<span data-ttu-id="966c7-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966c7-128">-주제</span><span class="sxs-lookup"><span data-stu-id="966c7-128">-Topic</span></span>
<span data-ttu-id="966c7-129">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966c7-130">CommonParameters</span></span>
<span data-ttu-id="966c7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="966c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966c7-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="966c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966c7-133">입력</span><span class="sxs-lookup"><span data-stu-id="966c7-133">INPUTS</span></span>

### <span data-ttu-id="966c7-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="966c7-134">-ResourceGroup</span></span>
 <span data-ttu-id="966c7-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="966c7-135">System.String</span></span>
 

### <span data-ttu-id="966c7-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="966c7-136">-NamespaceName</span></span>
 <span data-ttu-id="966c7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="966c7-137">System.String</span></span>
 

### <span data-ttu-id="966c7-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="966c7-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="966c7-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="966c7-139">System.String</span></span>
 

### <span data-ttu-id="966c7-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="966c7-140">-TopicName</span></span>
 <span data-ttu-id="966c7-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="966c7-141">System.String</span></span>
 

### <span data-ttu-id="966c7-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="966c7-142">-RegenerateKeys</span></span>
 <span data-ttu-id="966c7-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="966c7-143">System.String</span></span>

## <span data-ttu-id="966c7-144">출력</span><span class="sxs-lookup"><span data-stu-id="966c7-144">OUTPUTS</span></span>

### <span data-ttu-id="966c7-145">ServiceBus. ListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="966c7-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="966c7-146">PrimaryConnectionString: 끝점 = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBTopicAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: Endpoint = SB://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBTopicAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-Topi c_exampl1 PrimaryKey: {PrimaryKey 값} SecondaryKey: {SecondaryKey 값} KeyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="966c7-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="966c7-147">상속자</span><span class="sxs-lookup"><span data-stu-id="966c7-147">NOTES</span></span>

## <span data-ttu-id="966c7-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="966c7-148">RELATED LINKS</span></span>

