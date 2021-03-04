---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: fc0cc8acf45403593124135cab87072a719f291d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961600"
---
# <span data-ttu-id="fc41b-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fc41b-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="fc41b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc41b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc41b-103">{{Synopsis}} 채우기}</span><span class="sxs-lookup"><span data-stu-id="fc41b-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="fc41b-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc41b-104">SYNTAX</span></span>

### <span data-ttu-id="fc41b-105">MigrationConfigurationPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc41b-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc41b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc41b-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc41b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc41b-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc41b-108">설명</span><span class="sxs-lookup"><span data-stu-id="fc41b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc41b-109">**Stop-AzServiceBusMigration** cmdlet은 표준 간 마이그레이션을 프리미엄 네임스페이스로 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="fc41b-110">예제</span><span class="sxs-lookup"><span data-stu-id="fc41b-110">EXAMPLES</span></span>

### <span data-ttu-id="fc41b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc41b-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="fc41b-112">Cmdlet은 마이그레이션 구성을 만드는 동안 제공된 표준 네임스페이스와 Premium 네임스페이스 간의 마이그레이션을 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="fc41b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc41b-113">PARAMETERS</span></span>

### <span data-ttu-id="fc41b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc41b-114">-DefaultProfile</span></span>
<span data-ttu-id="fc41b-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc41b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc41b-116">-InputObject</span></span>
<span data-ttu-id="fc41b-117">Service Bus 마이그레이션 구성 표준 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="fc41b-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc41b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fc41b-118">-Name</span></span>
<span data-ttu-id="fc41b-119">표준 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="fc41b-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc41b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc41b-120">-PassThru</span></span>
<span data-ttu-id="fc41b-121">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fc41b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc41b-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc41b-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fc41b-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc41b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc41b-124">-ResourceId</span></span>
<span data-ttu-id="fc41b-125">Service Bus 마이그레이션 구성 표준 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fc41b-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="fc41b-126">-확인</span><span class="sxs-lookup"><span data-stu-id="fc41b-126">-Confirm</span></span>
<span data-ttu-id="fc41b-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc41b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc41b-128">-WhatIf</span></span>
<span data-ttu-id="fc41b-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc41b-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc41b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc41b-131">CommonParameters</span></span>
<span data-ttu-id="fc41b-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc41b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc41b-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc41b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc41b-134">입력</span><span class="sxs-lookup"><span data-stu-id="fc41b-134">INPUTS</span></span>

### <span data-ttu-id="fc41b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fc41b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="fc41b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fc41b-136">System.String</span></span>

## <span data-ttu-id="fc41b-137">출력</span><span class="sxs-lookup"><span data-stu-id="fc41b-137">OUTPUTS</span></span>

### <span data-ttu-id="fc41b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc41b-138">System.Boolean</span></span>

## <span data-ttu-id="fc41b-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc41b-139">NOTES</span></span>

## <span data-ttu-id="fc41b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc41b-140">RELATED LINKS</span></span>
