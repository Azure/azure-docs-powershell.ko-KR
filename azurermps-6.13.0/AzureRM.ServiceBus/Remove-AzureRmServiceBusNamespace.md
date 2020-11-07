---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702447"
---
# <span data-ttu-id="dad56-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="dad56-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="dad56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad56-102">SYNOPSIS</span></span>
<span data-ttu-id="dad56-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dad56-104">SYNTAX</span></span>

### <span data-ttu-id="dad56-105">NamespacePropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dad56-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad56-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dad56-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad56-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dad56-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad56-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dad56-108">DESCRIPTION</span></span>
<span data-ttu-id="dad56-109">**AzureRmServiceBusNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="dad56-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dad56-110">EXAMPLES</span></span>

### <span data-ttu-id="dad56-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dad56-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="dad56-112">지정 된 리소스 그룹에서 서비스 버스 네임 스페이스를 제거 `SB-Example1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="dad56-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="dad56-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="dad56-114">$Inputobject를 통해 제공 되는 서비스 버스 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="dad56-115">예제 2.2-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="dad56-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="dad56-116">파이핑을 사용 하 여 Service Bus 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="dad56-117">예제 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dad56-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="dad56-118">-ResourceId 매개 변수 또는 파이프를 통해 $resourceid ARM id를 통해 제공 된 서비스 버스 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="dad56-119">변수</span><span class="sxs-lookup"><span data-stu-id="dad56-119">PARAMETERS</span></span>

### <span data-ttu-id="dad56-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad56-120">-AsJob</span></span>
<span data-ttu-id="dad56-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dad56-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dad56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad56-122">-DefaultProfile</span></span>
<span data-ttu-id="dad56-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad56-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dad56-124">-InputObject</span></span>
<span data-ttu-id="dad56-125">Service Bus 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="dad56-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="dad56-126">-이름</span><span class="sxs-lookup"><span data-stu-id="dad56-126">-Name</span></span>
<span data-ttu-id="dad56-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-127">Namespace Name.</span></span>

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

### <span data-ttu-id="dad56-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dad56-128">-PassThru</span></span>
<span data-ttu-id="dad56-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dad56-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad56-130">-ResourceGroupName</span></span>
<span data-ttu-id="dad56-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-131">The name of the resource group</span></span>

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

### <span data-ttu-id="dad56-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dad56-132">-ResourceId</span></span>
<span data-ttu-id="dad56-133">Service Bus 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="dad56-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="dad56-134">-확인</span><span class="sxs-lookup"><span data-stu-id="dad56-134">-Confirm</span></span>
<span data-ttu-id="dad56-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad56-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad56-136">-WhatIf</span></span>
<span data-ttu-id="dad56-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad56-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad56-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad56-139">CommonParameters</span></span>
<span data-ttu-id="dad56-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad56-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad56-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad56-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad56-142">입력</span><span class="sxs-lookup"><span data-stu-id="dad56-142">INPUTS</span></span>

### <span data-ttu-id="dad56-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dad56-143">System.String</span></span>

### <span data-ttu-id="dad56-144">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="dad56-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="dad56-145">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dad56-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dad56-146">출력</span><span class="sxs-lookup"><span data-stu-id="dad56-146">OUTPUTS</span></span>

### <span data-ttu-id="dad56-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dad56-147">System.Boolean</span></span>

## <span data-ttu-id="dad56-148">상속자</span><span class="sxs-lookup"><span data-stu-id="dad56-148">NOTES</span></span>

## <span data-ttu-id="dad56-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dad56-149">RELATED LINKS</span></span>
