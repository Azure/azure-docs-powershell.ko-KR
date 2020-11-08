---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204851"
---
# <span data-ttu-id="c2b44-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="c2b44-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="c2b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b44-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b44-103">GEO DR 장애 조치를 호출 하 고 보조 네임 스페이스를 가리키도록 별칭을 다시 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c2b44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2b44-104">SYNTAX</span></span>

### <span data-ttu-id="c2b44-105">Geodr속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2b44-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b44-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2b44-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b44-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b44-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b44-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2b44-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b44-109">**AzServiceBusGeoDRConfigurationFailOver** CMDLET은 GEO DR 장애 조치를 호출 하 고 보조 네임 스페이스를 가리키도록 별칭을 다시 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c2b44-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2b44-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b44-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2b44-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="c2b44-112">"SampleDRConfigName" 별칭을 통해 장애 조치를 호출 하 고, 재구성 하 고 보조 네임 스페이스 "SampleNamespace_Secondary"를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="c2b44-113">변수</span><span class="sxs-lookup"><span data-stu-id="c2b44-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b44-114">-DefaultProfile</span></span>
<span data-ttu-id="c2b44-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b44-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2b44-116">-InputObject</span></span>
<span data-ttu-id="c2b44-117">Service Bus GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="c2b44-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b44-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c2b44-118">-Name</span></span>
<span data-ttu-id="c2b44-119">DR 구성 이름-별칭</span><span class="sxs-lookup"><span data-stu-id="c2b44-119">DR Configuration Name - Alias</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b44-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c2b44-120">-Namespace</span></span>
<span data-ttu-id="c2b44-121">네임 스페이스 이름-보조 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="c2b44-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b44-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2b44-122">-PassThru</span></span>
<span data-ttu-id="c2b44-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c2b44-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b44-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2b44-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c2b44-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b44-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b44-127">-ResourceId</span></span>
<span data-ttu-id="c2b44-128">GeoDRConfiguration 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c2b44-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b44-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c2b44-129">-Confirm</span></span>
<span data-ttu-id="c2b44-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b44-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b44-131">-WhatIf</span></span>
<span data-ttu-id="c2b44-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b44-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b44-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b44-134">CommonParameters</span></span>
<span data-ttu-id="c2b44-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b44-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b44-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b44-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b44-137">입력</span><span class="sxs-lookup"><span data-stu-id="c2b44-137">INPUTS</span></span>

### <span data-ttu-id="c2b44-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2b44-138">System.String</span></span>

### <span data-ttu-id="c2b44-139">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c2b44-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c2b44-140">출력</span><span class="sxs-lookup"><span data-stu-id="c2b44-140">OUTPUTS</span></span>

### <span data-ttu-id="c2b44-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c2b44-141">System.Boolean</span></span>

## <span data-ttu-id="c2b44-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c2b44-142">NOTES</span></span>

## <span data-ttu-id="c2b44-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2b44-143">RELATED LINKS</span></span>
