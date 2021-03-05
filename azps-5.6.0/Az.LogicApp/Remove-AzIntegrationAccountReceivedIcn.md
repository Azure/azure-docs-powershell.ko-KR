---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: a87ccecbba21479c24a2defd2d7443f66184a799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961931"
---
# <span data-ttu-id="7653a-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="7653a-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="7653a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7653a-102">SYNOPSIS</span></span>
<span data-ttu-id="7653a-103">이 cmdlet은 계약당 특정 교환 제어 번호 및 제어 번호 값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="7653a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7653a-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7653a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7653a-105">DESCRIPTION</span></span>
<span data-ttu-id="7653a-106">이 cmdlet은 재해 복구 시나리오에서 B2B 커넥터가 중복 번호 검색을 사용하도록 설정하면 메시지를 다시 처리할 수 있도록 통합 계정에서 받은 교환 제어 번호를 제거하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="7653a-107">드문 경우로 수신된 교환 제어 번호는 재해 직전 및 B2B 커넥터가 교환을 부적당하게 거부하기 전에 예약될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="7653a-108">이러한 경우 작업은 페이로드가 수정된 후에 복구 사이트가 동일한 교환을 다시 처리하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="7653a-109">반환할 X12 또는 Edifact 제어 번호 여부를 지정하기 위해 "-AgreementType" 매개 변수를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="7653a-110">예제</span><span class="sxs-lookup"><span data-stu-id="7653a-110">EXAMPLES</span></span>

### <span data-ttu-id="7653a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7653a-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="7653a-112">콘텐츠가 유효한 형식이 아닌 수신된 X12 교환 제어 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="7653a-113">받은 X12 교환 제어 번호를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="7653a-114">받은 X12 교환 제어 번호가 다시 시도하여 제거된지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="7653a-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="7653a-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="7653a-116">콘텐츠가 유효한 형식이 아닌 수신된 Edifact 교환 제어 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="7653a-117">수신된 Edifact 교환 제어 번호를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="7653a-118">수신된 Edifact 교환 제어 번호가 다시 시도하여 제거된지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="7653a-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7653a-119">PARAMETERS</span></span>

### <span data-ttu-id="7653a-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7653a-120">-AgreementName</span></span>
<span data-ttu-id="7653a-121">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-121">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="7653a-122">-AgreementType</span></span>
<span data-ttu-id="7653a-123">통합 계정 계약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="7653a-124">-ControlNumberValue</span></span>
<span data-ttu-id="7653a-125">통합 계정 제어 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-125">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7653a-126">-DefaultProfile</span></span>
<span data-ttu-id="7653a-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7653a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7653a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7653a-128">-Name</span></span>
<span data-ttu-id="7653a-129">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7653a-130">-ResourceGroupName</span></span>
<span data-ttu-id="7653a-131">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-131">The integration account resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7653a-132">-Confirm</span></span>
<span data-ttu-id="7653a-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7653a-134">-WhatIf</span></span>
<span data-ttu-id="7653a-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7653a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7653a-137">CommonParameters</span></span>
<span data-ttu-id="7653a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7653a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7653a-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7653a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7653a-140">입력</span><span class="sxs-lookup"><span data-stu-id="7653a-140">INPUTS</span></span>

### <span data-ttu-id="7653a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7653a-141">System.String</span></span>

## <span data-ttu-id="7653a-142">출력</span><span class="sxs-lookup"><span data-stu-id="7653a-142">OUTPUTS</span></span>

### <span data-ttu-id="7653a-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="7653a-143">System.Void</span></span>

## <span data-ttu-id="7653a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7653a-144">NOTES</span></span>

## <span data-ttu-id="7653a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7653a-145">RELATED LINKS</span></span>

<span data-ttu-id="7653a-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="7653a-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

