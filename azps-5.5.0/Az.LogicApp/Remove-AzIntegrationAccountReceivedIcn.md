---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187572"
---
# <span data-ttu-id="df13b-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="df13b-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="df13b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df13b-102">SYNOPSIS</span></span>
<span data-ttu-id="df13b-103">이 cmdlet은 규약당 특정 받은 교환 컨트롤 번호 및 컨트롤 번호 값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="df13b-104">구문</span><span class="sxs-lookup"><span data-stu-id="df13b-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df13b-105">설명</span><span class="sxs-lookup"><span data-stu-id="df13b-105">DESCRIPTION</span></span>
<span data-ttu-id="df13b-106">이 cmdlet은 B2B 커넥터가 중복 번호 검색을 사용할 때 메시지를 다시 처리하기 위해 통합 계정에서 수신된 교환 제어 번호를 제거하는 재해 복구 시나리오에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="df13b-107">드물게 수신된 교환 컨트롤 번호는 재해 직전 및 B2B 커넥터가 교환을 오타로 거부하기 전에 예약될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="df13b-108">이러한 경우 작업은 복구 사이트가 페이로드가 수정된 후 동일한 교환을 다시 처리하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="df13b-109">"-AgreementType" 매개 변수를 제공하여 X12 또는 Edifact 컨트롤 번호가 반환될지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="df13b-110">예제</span><span class="sxs-lookup"><span data-stu-id="df13b-110">EXAMPLES</span></span>

### <span data-ttu-id="df13b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="df13b-111">Example 1</span></span>
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

<span data-ttu-id="df13b-112">콘텐츠가 유효한 형식이 아닌 수신된 X12 교환 컨트롤 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="df13b-113">받은 X12 교환 컨트롤 번호를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="df13b-114">받은 X12 교환 컨트롤 번호를 다시 시도하여 제거된지 확인</span><span class="sxs-lookup"><span data-stu-id="df13b-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="df13b-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="df13b-115">Example 2</span></span>
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

<span data-ttu-id="df13b-116">콘텐츠가 유효한 형식이 아닌 수신된 Edifact 교환 컨트롤 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="df13b-117">받은 Edifact 교환 컨트롤 번호를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="df13b-118">받은 Edifact 교환 컨트롤 번호를 다시 시도하여 제거된지 확인</span><span class="sxs-lookup"><span data-stu-id="df13b-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="df13b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df13b-119">PARAMETERS</span></span>

### <span data-ttu-id="df13b-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="df13b-120">-AgreementName</span></span>
<span data-ttu-id="df13b-121">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="df13b-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="df13b-122">-AgreementType</span></span>
<span data-ttu-id="df13b-123">통합 계정 계약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="df13b-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="df13b-124">-ControlNumberValue</span></span>
<span data-ttu-id="df13b-125">통합 계정 컨트롤 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="df13b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df13b-126">-DefaultProfile</span></span>
<span data-ttu-id="df13b-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="df13b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df13b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="df13b-128">-Name</span></span>
<span data-ttu-id="df13b-129">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-129">The integration account name.</span></span>

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

### <span data-ttu-id="df13b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df13b-130">-ResourceGroupName</span></span>
<span data-ttu-id="df13b-131">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="df13b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df13b-132">-Confirm</span></span>
<span data-ttu-id="df13b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df13b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df13b-134">-WhatIf</span></span>
<span data-ttu-id="df13b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df13b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df13b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df13b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df13b-137">CommonParameters</span></span>
<span data-ttu-id="df13b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df13b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df13b-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df13b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df13b-140">입력</span><span class="sxs-lookup"><span data-stu-id="df13b-140">INPUTS</span></span>

### <span data-ttu-id="df13b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="df13b-141">System.String</span></span>

## <span data-ttu-id="df13b-142">출력</span><span class="sxs-lookup"><span data-stu-id="df13b-142">OUTPUTS</span></span>

### <span data-ttu-id="df13b-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="df13b-143">System.Void</span></span>

## <span data-ttu-id="df13b-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df13b-144">NOTES</span></span>

## <span data-ttu-id="df13b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df13b-145">RELATED LINKS</span></span>

<span data-ttu-id="df13b-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="df13b-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

