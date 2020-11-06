---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532166"
---
# <span data-ttu-id="8227a-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="8227a-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="8227a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8227a-102">SYNOPSIS</span></span>
<span data-ttu-id="8227a-103">이벤트 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8227a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8227a-104">SYNTAX</span></span>

### <span data-ttu-id="8227a-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8227a-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8227a-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8227a-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8227a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8227a-107">DESCRIPTION</span></span>
<span data-ttu-id="8227a-108">New-AzureRmEventHubNamespace cmdlet은 이벤트 허브 유형의 새 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="8227a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8227a-109">EXAMPLES</span></span>

### <span data-ttu-id="8227a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8227a-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="8227a-111">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 Mylocation에 이벤트 \` 허브 네임 스페이스 MyNamespaceName를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="8227a-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8227a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8227a-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="8227a-113">\`지정 된 지리적 위치 mylocation에 이벤트 허브 네임 스페이스 MyNamespaceName를 만들고 \` \` \` , 리소스 그룹 \` MyResourceGroupName에서 \` MaximumThroughputUnits 10으로 autoinflate을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="8227a-114">변수</span><span class="sxs-lookup"><span data-stu-id="8227a-114">PARAMETERS</span></span>

### <span data-ttu-id="8227a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8227a-115">-DefaultProfile</span></span>
<span data-ttu-id="8227a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8227a-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="8227a-117">-EnableAutoInflate</span></span>
<span data-ttu-id="8227a-118">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-119">-위치</span><span class="sxs-lookup"><span data-stu-id="8227a-119">-Location</span></span>
<span data-ttu-id="8227a-120">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="8227a-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="8227a-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="8227a-122">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8227a-123">-Name</span></span>
<span data-ttu-id="8227a-124">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8227a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8227a-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8227a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8227a-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8227a-127">-SkuCapacity</span></span>
<span data-ttu-id="8227a-128">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-129">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="8227a-129">-SkuName</span></span>
<span data-ttu-id="8227a-130">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-130">Namespace Sku Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-131">태그</span><span class="sxs-lookup"><span data-stu-id="8227a-131">-Tag</span></span>
<span data-ttu-id="8227a-132">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="8227a-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-133">-확인</span><span class="sxs-lookup"><span data-stu-id="8227a-133">-Confirm</span></span>
<span data-ttu-id="8227a-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8227a-135">-WhatIf</span></span>
<span data-ttu-id="8227a-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8227a-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8227a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8227a-138">CommonParameters</span></span>
<span data-ttu-id="8227a-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8227a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8227a-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8227a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8227a-141">입력</span><span class="sxs-lookup"><span data-stu-id="8227a-141">INPUTS</span></span>

### <span data-ttu-id="8227a-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8227a-142">System.String</span></span>
<span data-ttu-id="8227a-143">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]] System.webserver. 컬렉션</span><span class="sxs-lookup"><span data-stu-id="8227a-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="8227a-144">출력</span><span class="sxs-lookup"><span data-stu-id="8227a-144">OUTPUTS</span></span>

### <span data-ttu-id="8227a-145">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="8227a-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="8227a-146">상속자</span><span class="sxs-lookup"><span data-stu-id="8227a-146">NOTES</span></span>

## <span data-ttu-id="8227a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8227a-147">RELATED LINKS</span></span>
