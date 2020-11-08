---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213326"
---
# <span data-ttu-id="10ae4-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="10ae4-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="10ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="10ae4-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="10ae4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10ae4-104">SYNTAX</span></span>

### <span data-ttu-id="10ae4-105">NamespacePropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="10ae4-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ae4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10ae4-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ae4-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ae4-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ae4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="10ae4-108">DESCRIPTION</span></span>
<span data-ttu-id="10ae4-109">**AzServiceBusNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="10ae4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="10ae4-110">EXAMPLES</span></span>

### <span data-ttu-id="10ae4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="10ae4-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="10ae4-112">지정 된 리소스 그룹에서 서비스 버스 네임 스페이스를 제거 `SB-Example1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="10ae4-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="10ae4-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="10ae4-114">$Inputobject를 통해 제공 되는 서비스 버스 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="10ae4-115">예제 2.2-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="10ae4-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="10ae4-116">파이핑을 사용 하 여 Service Bus 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="10ae4-117">예제 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10ae4-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="10ae4-118">-ResourceId 매개 변수 또는 파이프를 통해 $resourceid ARM id를 통해 제공 된 서비스 버스 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="10ae4-119">변수</span><span class="sxs-lookup"><span data-stu-id="10ae4-119">PARAMETERS</span></span>

### <span data-ttu-id="10ae4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10ae4-120">-AsJob</span></span>
<span data-ttu-id="10ae4-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="10ae4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10ae4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ae4-122">-DefaultProfile</span></span>
<span data-ttu-id="10ae4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ae4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10ae4-124">-InputObject</span></span>
<span data-ttu-id="10ae4-125">Service Bus 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="10ae4-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ae4-126">-이름</span><span class="sxs-lookup"><span data-stu-id="10ae4-126">-Name</span></span>
<span data-ttu-id="10ae4-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10ae4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10ae4-128">-PassThru</span></span>
<span data-ttu-id="10ae4-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="10ae4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ae4-130">-ResourceGroupName</span></span>
<span data-ttu-id="10ae4-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10ae4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10ae4-132">-ResourceId</span></span>
<span data-ttu-id="10ae4-133">Service Bus 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="10ae4-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10ae4-134">-확인</span><span class="sxs-lookup"><span data-stu-id="10ae4-134">-Confirm</span></span>
<span data-ttu-id="10ae4-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ae4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ae4-136">-WhatIf</span></span>
<span data-ttu-id="10ae4-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ae4-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ae4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ae4-139">CommonParameters</span></span>
<span data-ttu-id="10ae4-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ae4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ae4-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ae4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ae4-142">입력</span><span class="sxs-lookup"><span data-stu-id="10ae4-142">INPUTS</span></span>

### <span data-ttu-id="10ae4-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10ae4-143">System.String</span></span>

### <span data-ttu-id="10ae4-144">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="10ae4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="10ae4-145">출력</span><span class="sxs-lookup"><span data-stu-id="10ae4-145">OUTPUTS</span></span>

### <span data-ttu-id="10ae4-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="10ae4-146">System.Boolean</span></span>

## <span data-ttu-id="10ae4-147">상속자</span><span class="sxs-lookup"><span data-stu-id="10ae4-147">NOTES</span></span>

## <span data-ttu-id="10ae4-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10ae4-148">RELATED LINKS</span></span>
