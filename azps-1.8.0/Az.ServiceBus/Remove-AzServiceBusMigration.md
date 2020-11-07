---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: eff58056393c499e15a7ddb4ab018b7ff6e383a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699167"
---
# <span data-ttu-id="ee29b-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ee29b-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="ee29b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee29b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee29b-103">Cmdlet이 표준 및 Premium 네임 스페이스에 대 한 마이그레이션 구성을 삭제 함</span><span class="sxs-lookup"><span data-stu-id="ee29b-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="ee29b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee29b-104">SYNTAX</span></span>

### <span data-ttu-id="ee29b-105">MigrationConfigurationPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee29b-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee29b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee29b-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee29b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee29b-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee29b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ee29b-108">DESCRIPTION</span></span>
<span data-ttu-id="ee29b-109">AzServiceBusMigration cmdlet은 표준에서 Premium 네임 스페이스에 대 한 마이그레이션 구성을 삭제 **함**</span><span class="sxs-lookup"><span data-stu-id="ee29b-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="ee29b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ee29b-110">EXAMPLES</span></span>

### <span data-ttu-id="ee29b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee29b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="ee29b-112">' TestingNamespaceStandardMirgation ' 마이그레이션 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="ee29b-113">변수</span><span class="sxs-lookup"><span data-stu-id="ee29b-113">PARAMETERS</span></span>

### <span data-ttu-id="ee29b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee29b-114">-AsJob</span></span>
<span data-ttu-id="ee29b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ee29b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee29b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee29b-116">-DefaultProfile</span></span>
<span data-ttu-id="ee29b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee29b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee29b-118">-InputObject</span></span>
<span data-ttu-id="ee29b-119">Service Bus 마이그레이션 표준 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="ee29b-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="ee29b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ee29b-120">-Name</span></span>
<span data-ttu-id="ee29b-121">표준 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ee29b-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="ee29b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee29b-122">-PassThru</span></span>
<span data-ttu-id="ee29b-123">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ee29b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee29b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee29b-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ee29b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="ee29b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee29b-126">-ResourceId</span></span>
<span data-ttu-id="ee29b-127">Service Bus 마이그레이션 표준 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ee29b-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="ee29b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ee29b-128">-Confirm</span></span>
<span data-ttu-id="ee29b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee29b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee29b-130">-WhatIf</span></span>
<span data-ttu-id="ee29b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee29b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee29b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee29b-133">CommonParameters</span></span>
<span data-ttu-id="ee29b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee29b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee29b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee29b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee29b-136">입력</span><span class="sxs-lookup"><span data-stu-id="ee29b-136">INPUTS</span></span>

### <span data-ttu-id="ee29b-137">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ee29b-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="ee29b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee29b-138">System.String</span></span>

## <span data-ttu-id="ee29b-139">출력</span><span class="sxs-lookup"><span data-stu-id="ee29b-139">OUTPUTS</span></span>

### <span data-ttu-id="ee29b-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ee29b-140">System.Boolean</span></span>

## <span data-ttu-id="ee29b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ee29b-141">NOTES</span></span>

## <span data-ttu-id="ee29b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee29b-142">RELATED LINKS</span></span>
