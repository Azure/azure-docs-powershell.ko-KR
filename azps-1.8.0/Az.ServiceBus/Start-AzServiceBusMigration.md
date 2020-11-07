---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699134"
---
# <span data-ttu-id="6d0ea-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6d0ea-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="6d0ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0ea-103">새 마이그레이션 구성을 만들고 표준에서 Premium 네임 스페이스로 엔터티 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="6d0ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d0ea-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d0ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d0ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6d0ea-106">**AzServiceBusMigration** cmdlet은 새 마이그레이션 구성을 만들고 표준에서 Premium 네임 스페이스로 엔터티 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="6d0ea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6d0ea-107">EXAMPLES</span></span>

### <span data-ttu-id="6d0ea-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d0ea-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="6d0ea-109">' TestingNamespaceStandardMirgation '에 대 한 새 마이그레이션 구성을 ' TestingNamespacePremiumMirgation ' 네임 스페이스에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="6d0ea-110">변수</span><span class="sxs-lookup"><span data-stu-id="6d0ea-110">PARAMETERS</span></span>

### <span data-ttu-id="6d0ea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d0ea-111">-AsJob</span></span>
<span data-ttu-id="6d0ea-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6d0ea-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d0ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0ea-113">-DefaultProfile</span></span>
<span data-ttu-id="6d0ea-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d0ea-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6d0ea-115">-Name</span></span>
<span data-ttu-id="6d0ea-116">표준 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="6d0ea-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="6d0ea-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="6d0ea-117">-PostMigrationName</span></span>
<span data-ttu-id="6d0ea-118">마이그레이션에 있는 해당 Rad 네임 스페이스에 대 한 마이그레이션 이후 이름</span><span class="sxs-lookup"><span data-stu-id="6d0ea-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="6d0ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d0ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d0ea-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6d0ea-120">Resource Group Name</span></span>

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

### <span data-ttu-id="6d0ea-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="6d0ea-121">-TargetNameSpace</span></span>
<span data-ttu-id="6d0ea-122">Premium 네임 스페이스 ARM Id</span><span class="sxs-lookup"><span data-stu-id="6d0ea-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="6d0ea-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6d0ea-123">-Confirm</span></span>
<span data-ttu-id="6d0ea-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d0ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d0ea-125">-WhatIf</span></span>
<span data-ttu-id="6d0ea-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d0ea-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d0ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0ea-128">CommonParameters</span></span>
<span data-ttu-id="6d0ea-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0ea-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d0ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0ea-131">입력</span><span class="sxs-lookup"><span data-stu-id="6d0ea-131">INPUTS</span></span>

### <span data-ttu-id="6d0ea-132">않아야</span><span class="sxs-lookup"><span data-stu-id="6d0ea-132">None</span></span>

## <span data-ttu-id="6d0ea-133">출력</span><span class="sxs-lookup"><span data-stu-id="6d0ea-133">OUTPUTS</span></span>

### <span data-ttu-id="6d0ea-134">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6d0ea-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="6d0ea-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6d0ea-135">NOTES</span></span>

## <span data-ttu-id="6d0ea-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d0ea-136">RELATED LINKS</span></span>
