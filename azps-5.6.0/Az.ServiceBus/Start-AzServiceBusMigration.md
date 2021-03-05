---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 010e54b21d4abb3068f62e561c002fed6ca734d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988806"
---
# <span data-ttu-id="1987d-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1987d-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="1987d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1987d-102">SYNOPSIS</span></span>
<span data-ttu-id="1987d-103">새 마이그레이션 구성을 만들고 표준에서 Premium 네임스페이스로 엔터티 마이그레이션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="1987d-104">구문</span><span class="sxs-lookup"><span data-stu-id="1987d-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1987d-105">설명</span><span class="sxs-lookup"><span data-stu-id="1987d-105">DESCRIPTION</span></span>
<span data-ttu-id="1987d-106">**Start-AzServiceBusMigration** cmdlet은 새 마이그레이션 구성을 만들고 표준에서 Premium 네임스페이스로 엔터티 마이그레이션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="1987d-107">예제</span><span class="sxs-lookup"><span data-stu-id="1987d-107">EXAMPLES</span></span>

### <span data-ttu-id="1987d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1987d-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="1987d-109">'TestingNamespaceStandardMigration'에 대한 새 마이그레이션 구성을 'TestingNamespacePremiumMigration' 네임스페이스로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="1987d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1987d-110">PARAMETERS</span></span>

### <span data-ttu-id="1987d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1987d-111">-AsJob</span></span>
<span data-ttu-id="1987d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1987d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1987d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1987d-113">-DefaultProfile</span></span>
<span data-ttu-id="1987d-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1987d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1987d-115">-Name</span></span>
<span data-ttu-id="1987d-116">표준 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="1987d-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1987d-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="1987d-117">-PostMigrationName</span></span>
<span data-ttu-id="1987d-118">마이그레이션의 표준 네임스페이스에 대한 마이그레이션 이름 후</span><span class="sxs-lookup"><span data-stu-id="1987d-118">Post Migration Name for Standard Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1987d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1987d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1987d-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1987d-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1987d-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="1987d-121">-TargetNameSpace</span></span>
<span data-ttu-id="1987d-122">Premium 네임스페이스 ARM ID</span><span class="sxs-lookup"><span data-stu-id="1987d-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1987d-123">-확인</span><span class="sxs-lookup"><span data-stu-id="1987d-123">-Confirm</span></span>
<span data-ttu-id="1987d-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1987d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1987d-125">-WhatIf</span></span>
<span data-ttu-id="1987d-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1987d-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1987d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1987d-128">CommonParameters</span></span>
<span data-ttu-id="1987d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1987d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1987d-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1987d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1987d-131">입력</span><span class="sxs-lookup"><span data-stu-id="1987d-131">INPUTS</span></span>

### <span data-ttu-id="1987d-132">없음</span><span class="sxs-lookup"><span data-stu-id="1987d-132">None</span></span>

## <span data-ttu-id="1987d-133">출력</span><span class="sxs-lookup"><span data-stu-id="1987d-133">OUTPUTS</span></span>

### <span data-ttu-id="1987d-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1987d-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="1987d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1987d-135">NOTES</span></span>

## <span data-ttu-id="1987d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1987d-136">RELATED LINKS</span></span>
