---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703799"
---
# <span data-ttu-id="c5c1c-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c5c1c-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="c5c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c1c-103">Cmdlet 표준 네임 스페이스의 완료 된 연결 문자열과 Premium 네임 스페이스를 가리키는 기본 네임 스페이스의 마이그레이션 설정</span><span class="sxs-lookup"><span data-stu-id="c5c1c-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5c1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5c1c-104">SYNTAX</span></span>

### <span data-ttu-id="c5c1c-105">MigrationConfigurationPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5c1c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c1c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5c1c-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c1c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c1c-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5c1c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c5c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c5c1c-109">**AzureRmServiceBusMigration** cmdlet은 표준 네임 스페이스의 완전 한 연결 문자열로 서 premium 네임 스페이스를 가리키는 표준에서 premium 네임 스페이스로의 마이그레이션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="c5c1c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c5c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c5c1c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5c1c-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="c5c1c-112">' NamespaceStandardMirgation ' 네임 스페이스의 마이그레이션을 완료로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="c5c1c-113">변수</span><span class="sxs-lookup"><span data-stu-id="c5c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="c5c1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c1c-114">-DefaultProfile</span></span>
<span data-ttu-id="c5c1c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5c1c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5c1c-116">-InputObject</span></span>
<span data-ttu-id="c5c1c-117">Service Bus 마이그레이션 구성-표준 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="c5c1c-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="c5c1c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c5c1c-118">-Name</span></span>
<span data-ttu-id="c5c1c-119">표준 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="c5c1c-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="c5c1c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5c1c-120">-PassThru</span></span>
<span data-ttu-id="c5c1c-121">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c5c1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5c1c-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c5c1c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c5c1c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c1c-124">-ResourceId</span></span>
<span data-ttu-id="c5c1c-125">Service Bus Migratio-표준 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c5c1c-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="c5c1c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c5c1c-126">-Confirm</span></span>
<span data-ttu-id="c5c1c-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c1c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c1c-128">-WhatIf</span></span>
<span data-ttu-id="c5c1c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c1c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5c1c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c1c-131">CommonParameters</span></span>
<span data-ttu-id="c5c1c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c1c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c1c-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c1c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c1c-134">입력</span><span class="sxs-lookup"><span data-stu-id="c5c1c-134">INPUTS</span></span>

### <span data-ttu-id="c5c1c-135">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c5c1c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="c5c1c-136">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5c1c-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c5c1c-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5c1c-137">System.String</span></span>

## <span data-ttu-id="c5c1c-138">출력</span><span class="sxs-lookup"><span data-stu-id="c5c1c-138">OUTPUTS</span></span>

### <span data-ttu-id="c5c1c-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c5c1c-139">System.Boolean</span></span>

## <span data-ttu-id="c5c1c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c5c1c-140">NOTES</span></span>

## <span data-ttu-id="c5c1c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5c1c-141">RELATED LINKS</span></span>
