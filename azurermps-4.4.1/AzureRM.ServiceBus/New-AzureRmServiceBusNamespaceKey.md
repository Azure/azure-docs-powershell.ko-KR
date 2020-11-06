---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532928"
---
# <span data-ttu-id="424ff-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="424ff-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="424ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424ff-102">SYNOPSIS</span></span>
<span data-ttu-id="424ff-103">Service Bus 네임 스페이스에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="424ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="424ff-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="424ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="424ff-105">DESCRIPTION</span></span>
<span data-ttu-id="424ff-106">**새 AzureRmServiceBusNamespace** cmdlet은 지정 된 네임 스페이스 및 권한 부여 규칙에 대 한 새 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="424ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="424ff-107">EXAMPLES</span></span>

### <span data-ttu-id="424ff-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="424ff-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="424ff-109">네임 스페이스에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="424ff-110">변수</span><span class="sxs-lookup"><span data-stu-id="424ff-110">PARAMETERS</span></span>

### <span data-ttu-id="424ff-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="424ff-111">-RegenerateKeys</span></span>
<span data-ttu-id="424ff-112">키 재생성: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="424ff-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="424ff-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="424ff-113">-ResourceGroup</span></span>
<span data-ttu-id="424ff-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424ff-115">-확인</span><span class="sxs-lookup"><span data-stu-id="424ff-115">-Confirm</span></span>
<span data-ttu-id="424ff-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424ff-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424ff-117">-WhatIf</span></span>
<span data-ttu-id="424ff-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424ff-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424ff-120">-DefaultProfile</span></span>
<span data-ttu-id="424ff-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="424ff-122">-이름</span><span class="sxs-lookup"><span data-stu-id="424ff-122">-Name</span></span>
<span data-ttu-id="424ff-123">권한 부여 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="424ff-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="424ff-124">-Namespace</span></span>
<span data-ttu-id="424ff-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-125">Namespace Name.</span></span>

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

### <span data-ttu-id="424ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424ff-126">CommonParameters</span></span>
<span data-ttu-id="424ff-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="424ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424ff-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424ff-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424ff-129">입력</span><span class="sxs-lookup"><span data-stu-id="424ff-129">INPUTS</span></span>

### <span data-ttu-id="424ff-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="424ff-130">-ResourceGroup</span></span>
 <span data-ttu-id="424ff-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="424ff-131">System.String</span></span>
 

### <span data-ttu-id="424ff-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="424ff-132">-NamespaceName</span></span>
 <span data-ttu-id="424ff-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="424ff-133">System.String</span></span>
 

### <span data-ttu-id="424ff-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="424ff-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="424ff-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="424ff-135">System.String</span></span>
 

### <span data-ttu-id="424ff-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="424ff-136">-RegenerateKeys</span></span>
 <span data-ttu-id="424ff-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="424ff-137">System.String</span></span>

## <span data-ttu-id="424ff-138">출력</span><span class="sxs-lookup"><span data-stu-id="424ff-138">OUTPUTS</span></span>

### <span data-ttu-id="424ff-139">ServiceBus-. m m g 목록 키</span><span class="sxs-lookup"><span data-stu-id="424ff-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="424ff-140">PrimaryConnectionString: 끝점 = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = {SharedAccessKey-value} SecondaryConnectionString: Endpoint = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = {SharedAccessKey-value} PrimaryKey: {PrimaryKey 값} SecondaryKey: {SecondaryKey 값} KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="424ff-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="424ff-141">상속자</span><span class="sxs-lookup"><span data-stu-id="424ff-141">NOTES</span></span>

## <span data-ttu-id="424ff-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="424ff-142">RELATED LINKS</span></span>

