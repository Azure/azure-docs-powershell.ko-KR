---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178593"
---
# <span data-ttu-id="2e9ae-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2e9ae-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="2e9ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9ae-103">Cmdlet은 표준에서 프리미엄 네임스페이스로 마이그레이션을 완료로 설정하고 표준 네임스페이스의 연결 문자열은 이제 프리미엄 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="2e9ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e9ae-104">SYNTAX</span></span>

### <span data-ttu-id="2e9ae-105">MigrationConfigurationPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2e9ae-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9ae-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e9ae-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9ae-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e9ae-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e9ae-108">설명</span><span class="sxs-lookup"><span data-stu-id="2e9ae-108">DESCRIPTION</span></span>
<span data-ttu-id="2e9ae-109">**Complete-AzServiceBusMigration** cmdlet은 표준에서 프리미엄 네임스페이스로 마이그레이션을 완료로 설정하고 표준 네임스페이스의 연결 문자열은 이제 프리미엄 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="2e9ae-110">예제</span><span class="sxs-lookup"><span data-stu-id="2e9ae-110">EXAMPLES</span></span>

### <span data-ttu-id="2e9ae-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2e9ae-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="2e9ae-112">'NamespaceStandardMigration' 네임스페이스의 마이그레이션을 완료로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="2e9ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e9ae-113">PARAMETERS</span></span>

### <span data-ttu-id="2e9ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9ae-114">-DefaultProfile</span></span>
<span data-ttu-id="2e9ae-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e9ae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e9ae-116">-InputObject</span></span>
<span data-ttu-id="2e9ae-117">Service Bus 마이그레이션 구성 - 표준 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="2e9ae-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="2e9ae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2e9ae-118">-Name</span></span>
<span data-ttu-id="2e9ae-119">표준 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2e9ae-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="2e9ae-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e9ae-120">-PassThru</span></span>
<span data-ttu-id="2e9ae-121">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2e9ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e9ae-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e9ae-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2e9ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e9ae-124">-ResourceId</span></span>
<span data-ttu-id="2e9ae-125">Service Bus 마이그레이션 - 표준 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2e9ae-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="2e9ae-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e9ae-126">-Confirm</span></span>
<span data-ttu-id="2e9ae-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e9ae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e9ae-128">-WhatIf</span></span>
<span data-ttu-id="2e9ae-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2e9ae-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e9ae-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e9ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9ae-131">CommonParameters</span></span>
<span data-ttu-id="2e9ae-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9ae-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2e9ae-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9ae-134">입력</span><span class="sxs-lookup"><span data-stu-id="2e9ae-134">INPUTS</span></span>

### <span data-ttu-id="2e9ae-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2e9ae-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="2e9ae-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2e9ae-136">System.String</span></span>

## <span data-ttu-id="2e9ae-137">출력</span><span class="sxs-lookup"><span data-stu-id="2e9ae-137">OUTPUTS</span></span>

### <span data-ttu-id="2e9ae-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e9ae-138">System.Boolean</span></span>

## <span data-ttu-id="2e9ae-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e9ae-139">NOTES</span></span>

## <span data-ttu-id="2e9ae-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e9ae-140">RELATED LINKS</span></span>
