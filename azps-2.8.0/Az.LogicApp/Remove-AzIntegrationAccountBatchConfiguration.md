---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: e2c4f3f399bd4bcd472ae04c6ca2234c2d2b26d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689495"
---
# <span data-ttu-id="9530b-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9530b-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9530b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9530b-102">SYNOPSIS</span></span>
<span data-ttu-id="9530b-103">통합 계정 일괄 처리 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="9530b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9530b-104">SYNTAX</span></span>

### <span data-ttu-id="9530b-105">ByIntegrationAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="9530b-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9530b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9530b-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9530b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9530b-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9530b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9530b-108">DESCRIPTION</span></span>
<span data-ttu-id="9530b-109">**AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정에서 일괄 처리 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="9530b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9530b-110">EXAMPLES</span></span>

### <span data-ttu-id="9530b-111">예제 1: 매개 변수를 기준으로 일괄 처리 구성 제거</span><span class="sxs-lookup"><span data-stu-id="9530b-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="9530b-112">통합 계정 "sampleIntegrationAccount"에 있는 "sampleBatchConfig" 이라는 일괄 처리 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="9530b-113">변수</span><span class="sxs-lookup"><span data-stu-id="9530b-113">PARAMETERS</span></span>

### <span data-ttu-id="9530b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9530b-114">-DefaultProfile</span></span>
<span data-ttu-id="9530b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9530b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9530b-116">-InputObject</span></span>
<span data-ttu-id="9530b-117">통합 계정 일괄 처리 구성.</span><span class="sxs-lookup"><span data-stu-id="9530b-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9530b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9530b-118">-Name</span></span>
<span data-ttu-id="9530b-119">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9530b-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="9530b-120">-ParentName</span></span>
<span data-ttu-id="9530b-121">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9530b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9530b-122">-PassThru</span></span>
<span data-ttu-id="9530b-123">명령이 성공적으로 실행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="9530b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9530b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9530b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9530b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9530b-126">-ResourceId</span></span>
<span data-ttu-id="9530b-127">통합 계정 일괄 처리 구성 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9530b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9530b-128">-Confirm</span></span>
<span data-ttu-id="9530b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9530b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9530b-130">-WhatIf</span></span>
<span data-ttu-id="9530b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9530b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9530b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9530b-133">CommonParameters</span></span>
<span data-ttu-id="9530b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9530b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9530b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9530b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9530b-136">입력</span><span class="sxs-lookup"><span data-stu-id="9530b-136">INPUTS</span></span>

### <span data-ttu-id="9530b-137">LogicApp. PSIntegrationAccountBatchConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="9530b-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="9530b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9530b-138">System.String</span></span>

## <span data-ttu-id="9530b-139">출력</span><span class="sxs-lookup"><span data-stu-id="9530b-139">OUTPUTS</span></span>

### <span data-ttu-id="9530b-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9530b-140">System.Boolean</span></span>

## <span data-ttu-id="9530b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9530b-141">NOTES</span></span>

## <span data-ttu-id="9530b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9530b-142">RELATED LINKS</span></span>
