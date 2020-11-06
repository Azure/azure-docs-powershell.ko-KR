---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530892"
---
# <span data-ttu-id="13279-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="13279-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="13279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13279-102">SYNOPSIS</span></span>
<span data-ttu-id="13279-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="13279-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13279-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13279-104">SYNTAX</span></span>

### <span data-ttu-id="13279-105">MigrationConfigurationPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="13279-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13279-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13279-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13279-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13279-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13279-108">설명은</span><span class="sxs-lookup"><span data-stu-id="13279-108">DESCRIPTION</span></span>
<span data-ttu-id="13279-109">**AzureRmServiceBusMigration** Cmdlet은 표준 ~ premium 네임 스페이스 간 마이그레이션을 tremitates 합니다.</span><span class="sxs-lookup"><span data-stu-id="13279-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="13279-110">예제의</span><span class="sxs-lookup"><span data-stu-id="13279-110">EXAMPLES</span></span>

### <span data-ttu-id="13279-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="13279-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="13279-112">cmdlet은 마이그레이션 구성을 만드는 동안 제공 되는 표준 네임 스페이스와 Premium 네임 스페이스 간의 마이그레이션을 termitates.</span><span class="sxs-lookup"><span data-stu-id="13279-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="13279-113">변수</span><span class="sxs-lookup"><span data-stu-id="13279-113">PARAMETERS</span></span>

### <span data-ttu-id="13279-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13279-114">-DefaultProfile</span></span>
<span data-ttu-id="13279-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13279-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13279-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13279-116">-InputObject</span></span>
<span data-ttu-id="13279-117">Service Bus 마이그레이션 구성 표준 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="13279-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="13279-118">-이름</span><span class="sxs-lookup"><span data-stu-id="13279-118">-Name</span></span>
<span data-ttu-id="13279-119">표준 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="13279-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="13279-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13279-120">-PassThru</span></span>
<span data-ttu-id="13279-121">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13279-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="13279-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13279-122">-ResourceGroupName</span></span>
<span data-ttu-id="13279-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="13279-123">Resource Group Name</span></span>

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

### <span data-ttu-id="13279-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13279-124">-ResourceId</span></span>
<span data-ttu-id="13279-125">Service Bus 마이그레이션 구성 표준 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="13279-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="13279-126">-확인</span><span class="sxs-lookup"><span data-stu-id="13279-126">-Confirm</span></span>
<span data-ttu-id="13279-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13279-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13279-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13279-128">-WhatIf</span></span>
<span data-ttu-id="13279-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13279-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13279-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13279-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13279-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13279-131">CommonParameters</span></span>
<span data-ttu-id="13279-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13279-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13279-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13279-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13279-134">입력</span><span class="sxs-lookup"><span data-stu-id="13279-134">INPUTS</span></span>

### <span data-ttu-id="13279-135">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="13279-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="13279-136">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13279-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="13279-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13279-137">System.String</span></span>

## <span data-ttu-id="13279-138">출력</span><span class="sxs-lookup"><span data-stu-id="13279-138">OUTPUTS</span></span>

### <span data-ttu-id="13279-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="13279-139">System.Boolean</span></span>

## <span data-ttu-id="13279-140">상속자</span><span class="sxs-lookup"><span data-stu-id="13279-140">NOTES</span></span>

## <span data-ttu-id="13279-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13279-141">RELATED LINKS</span></span>
