---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 1e782c381ec10d03f269fc0a2d0871f064e4ddef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871633"
---
# <span data-ttu-id="cd1d3-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cd1d3-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="cd1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1d3-103">네임 스페이스의 MigrationConfiguration를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="cd1d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd1d3-104">SYNTAX</span></span>

### <span data-ttu-id="cd1d3-105">MigrationConfigurationPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd1d3-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd1d3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd1d3-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd1d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd1d3-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd1d3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cd1d3-108">DESCRIPTION</span></span>
<span data-ttu-id="cd1d3-109">**AzServiceBusMigration** 는 네임 스페이스에 대 한 마이그레이션 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="cd1d3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cd1d3-110">EXAMPLES</span></span>

### <span data-ttu-id="cd1d3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd1d3-111">Example 1</span></span>
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

<span data-ttu-id="cd1d3-112">' TestingNamespaceStandardMigration '의 마이그레이션 구성 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="cd1d3-113">변수</span><span class="sxs-lookup"><span data-stu-id="cd1d3-113">PARAMETERS</span></span>

### <span data-ttu-id="cd1d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1d3-114">-DefaultProfile</span></span>
<span data-ttu-id="cd1d3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd1d3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd1d3-116">-InputObject</span></span>
<span data-ttu-id="cd1d3-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="cd1d3-117">Namespace Object</span></span>

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

### <span data-ttu-id="cd1d3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="cd1d3-118">-Name</span></span>
<span data-ttu-id="cd1d3-119">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="cd1d3-119">Namespace Name</span></span>

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

### <span data-ttu-id="cd1d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd1d3-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cd1d3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="cd1d3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd1d3-122">-ResourceId</span></span>
<span data-ttu-id="cd1d3-123">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="cd1d3-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="cd1d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1d3-124">CommonParameters</span></span>
<span data-ttu-id="cd1d3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1d3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd1d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1d3-127">입력</span><span class="sxs-lookup"><span data-stu-id="cd1d3-127">INPUTS</span></span>

### <span data-ttu-id="cd1d3-128">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="cd1d3-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd1d3-129">System.String</span></span>

## <span data-ttu-id="cd1d3-130">출력</span><span class="sxs-lookup"><span data-stu-id="cd1d3-130">OUTPUTS</span></span>

### <span data-ttu-id="cd1d3-131">ServiceBus. PSServiceBusMigrationConfigurationAttributes/.</span><span class="sxs-lookup"><span data-stu-id="cd1d3-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="cd1d3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="cd1d3-132">NOTES</span></span>

## <span data-ttu-id="cd1d3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd1d3-133">RELATED LINKS</span></span>
