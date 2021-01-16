---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369069"
---
# <span data-ttu-id="ef3ef-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ef3ef-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="ef3ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3ef-103">{{동의어 채우기}}</span><span class="sxs-lookup"><span data-stu-id="ef3ef-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="ef3ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef3ef-104">SYNTAX</span></span>

### <span data-ttu-id="ef3ef-105">MigrationConfigurationPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef3ef-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3ef-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef3ef-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3ef-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef3ef-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3ef-108">설명</span><span class="sxs-lookup"><span data-stu-id="ef3ef-108">DESCRIPTION</span></span>
<span data-ttu-id="ef3ef-109">**Stop-AzServiceBusMigration** cmdlet은 표준에서 프리미엄 네임스페이스로의 마이그레이션을 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="ef3ef-110">예제</span><span class="sxs-lookup"><span data-stu-id="ef3ef-110">EXAMPLES</span></span>

### <span data-ttu-id="ef3ef-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef3ef-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="ef3ef-112">Cmdlet은 마이그레이션 구성을 만드는 동안 제공된 표준 네임스페이스와 프리미엄 네임스페이스 간의 마이그레이션을 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="ef3ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef3ef-113">PARAMETERS</span></span>

### <span data-ttu-id="ef3ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3ef-114">-DefaultProfile</span></span>
<span data-ttu-id="ef3ef-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef3ef-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef3ef-116">-InputObject</span></span>
<span data-ttu-id="ef3ef-117">Service Bus 마이그레이션 구성 표준 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="ef3ef-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="ef3ef-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ef3ef-118">-Name</span></span>
<span data-ttu-id="ef3ef-119">표준 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ef3ef-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="ef3ef-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef3ef-120">-PassThru</span></span>
<span data-ttu-id="ef3ef-121">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ef3ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef3ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef3ef-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ef3ef-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ef3ef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef3ef-124">-ResourceId</span></span>
<span data-ttu-id="ef3ef-125">Service Bus 마이그레이션 구성 표준 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ef3ef-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="ef3ef-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef3ef-126">-Confirm</span></span>
<span data-ttu-id="ef3ef-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3ef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3ef-128">-WhatIf</span></span>
<span data-ttu-id="ef3ef-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ef3ef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef3ef-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef3ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3ef-131">CommonParameters</span></span>
<span data-ttu-id="ef3ef-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3ef-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ef3ef-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3ef-134">입력</span><span class="sxs-lookup"><span data-stu-id="ef3ef-134">INPUTS</span></span>

### <span data-ttu-id="ef3ef-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ef3ef-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="ef3ef-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ef3ef-136">System.String</span></span>

## <span data-ttu-id="ef3ef-137">출력</span><span class="sxs-lookup"><span data-stu-id="ef3ef-137">OUTPUTS</span></span>

### <span data-ttu-id="ef3ef-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef3ef-138">System.Boolean</span></span>

## <span data-ttu-id="ef3ef-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef3ef-139">NOTES</span></span>

## <span data-ttu-id="ef3ef-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef3ef-140">RELATED LINKS</span></span>