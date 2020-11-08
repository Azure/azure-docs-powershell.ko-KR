---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044306"
---
# <span data-ttu-id="9870d-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9870d-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="9870d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9870d-102">SYNOPSIS</span></span>
<span data-ttu-id="9870d-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="9870d-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="9870d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9870d-104">SYNTAX</span></span>

### <span data-ttu-id="9870d-105">MigrationConfigurationPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9870d-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9870d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9870d-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9870d-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9870d-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9870d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9870d-108">DESCRIPTION</span></span>
<span data-ttu-id="9870d-109">**AzServiceBusMigration** Cmdlet이 표준 ~ premium 네임 스페이스 간의 마이그레이션을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="9870d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9870d-110">EXAMPLES</span></span>

### <span data-ttu-id="9870d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9870d-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="9870d-112">Cmdlet은 마이그레이션 구성을 만드는 동안 제공 된 표준 네임 스페이스와 Premium 네임 스페이스 간의 마이그레이션을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="9870d-113">변수</span><span class="sxs-lookup"><span data-stu-id="9870d-113">PARAMETERS</span></span>

### <span data-ttu-id="9870d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9870d-114">-DefaultProfile</span></span>
<span data-ttu-id="9870d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9870d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9870d-116">-InputObject</span></span>
<span data-ttu-id="9870d-117">Service Bus 마이그레이션 구성 표준 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="9870d-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="9870d-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9870d-118">-Name</span></span>
<span data-ttu-id="9870d-119">표준 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="9870d-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="9870d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9870d-120">-PassThru</span></span>
<span data-ttu-id="9870d-121">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9870d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9870d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9870d-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9870d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9870d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9870d-124">-ResourceId</span></span>
<span data-ttu-id="9870d-125">Service Bus 마이그레이션 구성 표준 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="9870d-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="9870d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9870d-126">-Confirm</span></span>
<span data-ttu-id="9870d-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9870d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9870d-128">-WhatIf</span></span>
<span data-ttu-id="9870d-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9870d-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9870d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9870d-131">CommonParameters</span></span>
<span data-ttu-id="9870d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9870d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9870d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9870d-134">입력</span><span class="sxs-lookup"><span data-stu-id="9870d-134">INPUTS</span></span>

### <span data-ttu-id="9870d-135">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9870d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="9870d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9870d-136">System.String</span></span>

## <span data-ttu-id="9870d-137">출력</span><span class="sxs-lookup"><span data-stu-id="9870d-137">OUTPUTS</span></span>

### <span data-ttu-id="9870d-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9870d-138">System.Boolean</span></span>

## <span data-ttu-id="9870d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="9870d-139">NOTES</span></span>

## <span data-ttu-id="9870d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9870d-140">RELATED LINKS</span></span>
