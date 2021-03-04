---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 9e53dab771486758cbd57c8f5c530a458df655d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950944"
---
# <span data-ttu-id="6c935-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c935-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="6c935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c935-102">SYNOPSIS</span></span>
<span data-ttu-id="6c935-103">Cmdlet은 표준에서 프리미엄 네임스페이스에 대한 마이그레이션 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="6c935-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c935-104">SYNTAX</span></span>

### <span data-ttu-id="6c935-105">MigrationConfigurationPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6c935-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c935-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6c935-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c935-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c935-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c935-108">설명</span><span class="sxs-lookup"><span data-stu-id="6c935-108">DESCRIPTION</span></span>
<span data-ttu-id="6c935-109">**Remove-AzServiceBusMigration** cmdlet은 Standard에서 Premium 네임스페이스에 대한 마이그레이션 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="6c935-110">예제</span><span class="sxs-lookup"><span data-stu-id="6c935-110">EXAMPLES</span></span>

### <span data-ttu-id="6c935-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c935-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="6c935-112">'TestingNamespaceStandardMigration' 마이그레이션 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="6c935-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6c935-113">PARAMETERS</span></span>

### <span data-ttu-id="6c935-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c935-114">-AsJob</span></span>
<span data-ttu-id="6c935-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6c935-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c935-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c935-116">-DefaultProfile</span></span>
<span data-ttu-id="6c935-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c935-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c935-118">-InputObject</span></span>
<span data-ttu-id="6c935-119">Service Bus 마이그레이션 표준 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="6c935-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="6c935-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6c935-120">-Name</span></span>
<span data-ttu-id="6c935-121">표준 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="6c935-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="6c935-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c935-122">-PassThru</span></span>
<span data-ttu-id="6c935-123">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6c935-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c935-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c935-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6c935-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c935-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c935-126">-ResourceId</span></span>
<span data-ttu-id="6c935-127">Service Bus 마이그레이션 표준 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6c935-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="6c935-128">-확인</span><span class="sxs-lookup"><span data-stu-id="6c935-128">-Confirm</span></span>
<span data-ttu-id="6c935-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c935-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c935-130">-WhatIf</span></span>
<span data-ttu-id="6c935-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c935-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c935-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c935-133">CommonParameters</span></span>
<span data-ttu-id="6c935-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c935-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c935-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6c935-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c935-136">입력</span><span class="sxs-lookup"><span data-stu-id="6c935-136">INPUTS</span></span>

### <span data-ttu-id="6c935-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6c935-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="6c935-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6c935-138">System.String</span></span>

## <span data-ttu-id="6c935-139">출력</span><span class="sxs-lookup"><span data-stu-id="6c935-139">OUTPUTS</span></span>

### <span data-ttu-id="6c935-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c935-140">System.Boolean</span></span>

## <span data-ttu-id="6c935-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c935-141">NOTES</span></span>

## <span data-ttu-id="6c935-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c935-142">RELATED LINKS</span></span>
