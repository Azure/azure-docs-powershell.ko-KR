---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530907"
---
# <span data-ttu-id="5ee13-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5ee13-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="5ee13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ee13-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee13-103">네임 스페이스의 MigrationConfiguration를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ee13-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ee13-104">SYNTAX</span></span>

### <span data-ttu-id="5ee13-105">MigrationConfigurationPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ee13-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ee13-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ee13-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ee13-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ee13-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ee13-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5ee13-108">DESCRIPTION</span></span>
<span data-ttu-id="5ee13-109">**AzureRmServiceBusMigration** 는 네임 스페이스에 대 한 마이그레이션 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ee13-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="5ee13-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5ee13-110">EXAMPLES</span></span>

### <span data-ttu-id="5ee13-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ee13-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="5ee13-112">' TestingNamespaceStandardMirgation '의 마이그레이션 구성 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ee13-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="5ee13-113">변수</span><span class="sxs-lookup"><span data-stu-id="5ee13-113">PARAMETERS</span></span>

### <span data-ttu-id="5ee13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee13-114">-DefaultProfile</span></span>
<span data-ttu-id="5ee13-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ee13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ee13-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ee13-116">-InputObject</span></span>
<span data-ttu-id="5ee13-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="5ee13-117">Namespace Object</span></span>

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

### <span data-ttu-id="5ee13-118">-이름</span><span class="sxs-lookup"><span data-stu-id="5ee13-118">-Name</span></span>
<span data-ttu-id="5ee13-119">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="5ee13-119">Namespace Name</span></span>

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

### <span data-ttu-id="5ee13-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee13-120">-ResourceGroupName</span></span>
<span data-ttu-id="5ee13-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5ee13-121">Resource Group Name</span></span>

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

### <span data-ttu-id="5ee13-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ee13-122">-ResourceId</span></span>
<span data-ttu-id="5ee13-123">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5ee13-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="5ee13-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee13-124">CommonParameters</span></span>
<span data-ttu-id="5ee13-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ee13-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee13-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee13-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee13-127">입력</span><span class="sxs-lookup"><span data-stu-id="5ee13-127">INPUTS</span></span>

### <span data-ttu-id="5ee13-128">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="5ee13-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="5ee13-129">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ee13-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5ee13-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ee13-130">System.String</span></span>

## <span data-ttu-id="5ee13-131">출력</span><span class="sxs-lookup"><span data-stu-id="5ee13-131">OUTPUTS</span></span>

### <span data-ttu-id="5ee13-132">ServiceBus. PSServiceBusMigrationConfigurationAttributes/.</span><span class="sxs-lookup"><span data-stu-id="5ee13-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="5ee13-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5ee13-133">NOTES</span></span>

## <span data-ttu-id="5ee13-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ee13-134">RELATED LINKS</span></span>
