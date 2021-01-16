---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343694"
---
# <span data-ttu-id="4f726-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4f726-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="4f726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f726-102">SYNOPSIS</span></span>
<span data-ttu-id="4f726-103">Cmdlet은 표준에서 프리미엄 네임스페이스로 마이그레이션을 완료로 설정하고 표준 네임스페이스의 연결 문자열은 이제 프리미엄 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="4f726-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f726-104">SYNTAX</span></span>

### <span data-ttu-id="4f726-105">MigrationConfigurationPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f726-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f726-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f726-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f726-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f726-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f726-108">설명</span><span class="sxs-lookup"><span data-stu-id="4f726-108">DESCRIPTION</span></span>
<span data-ttu-id="4f726-109">**Complete-AzServiceBusMigration** cmdlet은 표준에서 프리미엄 네임스페이스로 마이그레이션을 완료로 설정하고 표준 네임스페이스의 연결 문자열은 이제 프리미엄 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="4f726-110">예제</span><span class="sxs-lookup"><span data-stu-id="4f726-110">EXAMPLES</span></span>

### <span data-ttu-id="4f726-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f726-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="4f726-112">'NamespaceStandardMigration' 네임스페이스의 마이그레이션을 완료로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="4f726-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f726-113">PARAMETERS</span></span>

### <span data-ttu-id="4f726-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f726-114">-DefaultProfile</span></span>
<span data-ttu-id="4f726-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f726-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f726-116">-InputObject</span></span>
<span data-ttu-id="4f726-117">Service Bus 마이그레이션 구성 - 표준 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="4f726-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="4f726-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4f726-118">-Name</span></span>
<span data-ttu-id="4f726-119">표준 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="4f726-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="4f726-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f726-120">-PassThru</span></span>
<span data-ttu-id="4f726-121">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4f726-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f726-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f726-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4f726-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4f726-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f726-124">-ResourceId</span></span>
<span data-ttu-id="4f726-125">Service Bus 마이그레이션 - 표준 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4f726-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="4f726-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f726-126">-Confirm</span></span>
<span data-ttu-id="4f726-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f726-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f726-128">-WhatIf</span></span>
<span data-ttu-id="4f726-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4f726-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f726-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f726-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f726-131">CommonParameters</span></span>
<span data-ttu-id="4f726-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f726-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f726-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4f726-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f726-134">입력</span><span class="sxs-lookup"><span data-stu-id="4f726-134">INPUTS</span></span>

### <span data-ttu-id="4f726-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4f726-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="4f726-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4f726-136">System.String</span></span>

## <span data-ttu-id="4f726-137">출력</span><span class="sxs-lookup"><span data-stu-id="4f726-137">OUTPUTS</span></span>

### <span data-ttu-id="4f726-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f726-138">System.Boolean</span></span>

## <span data-ttu-id="4f726-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f726-139">NOTES</span></span>

## <span data-ttu-id="4f726-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f726-140">RELATED LINKS</span></span>
