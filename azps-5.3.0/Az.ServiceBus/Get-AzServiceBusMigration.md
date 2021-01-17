---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494892"
---
# <span data-ttu-id="31ff0-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31ff0-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="31ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="31ff0-103">네임스페이스에 대한 MigrationConfiguration을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="31ff0-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="31ff0-104">구문</span><span class="sxs-lookup"><span data-stu-id="31ff0-104">SYNTAX</span></span>

### <span data-ttu-id="31ff0-105">MigrationConfigurationPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="31ff0-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31ff0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31ff0-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31ff0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31ff0-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31ff0-108">설명</span><span class="sxs-lookup"><span data-stu-id="31ff0-108">DESCRIPTION</span></span>
<span data-ttu-id="31ff0-109">**Get-AzServiceBusMigration은** 네임스페이스에 대한 마이그레이션 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="31ff0-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="31ff0-110">예제</span><span class="sxs-lookup"><span data-stu-id="31ff0-110">EXAMPLES</span></span>

### <span data-ttu-id="31ff0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="31ff0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="31ff0-112">'TestingNamespaceStandardMigration'의 마이그레이션 구성 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31ff0-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="31ff0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31ff0-113">PARAMETERS</span></span>

### <span data-ttu-id="31ff0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ff0-114">-DefaultProfile</span></span>
<span data-ttu-id="31ff0-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31ff0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ff0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31ff0-116">-InputObject</span></span>
<span data-ttu-id="31ff0-117">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="31ff0-117">Namespace Object</span></span>

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

### <span data-ttu-id="31ff0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="31ff0-118">-Name</span></span>
<span data-ttu-id="31ff0-119">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="31ff0-119">Namespace Name</span></span>

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

### <span data-ttu-id="31ff0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ff0-120">-ResourceGroupName</span></span>
<span data-ttu-id="31ff0-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="31ff0-121">Resource Group Name</span></span>

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

### <span data-ttu-id="31ff0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31ff0-122">-ResourceId</span></span>
<span data-ttu-id="31ff0-123">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="31ff0-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ff0-124">CommonParameters</span></span>
<span data-ttu-id="31ff0-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31ff0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ff0-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31ff0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ff0-127">입력</span><span class="sxs-lookup"><span data-stu-id="31ff0-127">INPUTS</span></span>

### <span data-ttu-id="31ff0-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="31ff0-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="31ff0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="31ff0-129">System.String</span></span>

## <span data-ttu-id="31ff0-130">출력</span><span class="sxs-lookup"><span data-stu-id="31ff0-130">OUTPUTS</span></span>

### <span data-ttu-id="31ff0-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="31ff0-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="31ff0-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31ff0-132">NOTES</span></span>

## <span data-ttu-id="31ff0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31ff0-133">RELATED LINKS</span></span>
