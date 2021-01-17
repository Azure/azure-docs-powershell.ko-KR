---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490152"
---
# <span data-ttu-id="77ceb-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="77ceb-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="77ceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="77ceb-103">Azure 리소스 그룹에서 통합 계정이 받은 교환 제어 번호(ICN)를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="77ceb-104">구문</span><span class="sxs-lookup"><span data-stu-id="77ceb-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77ceb-105">설명</span><span class="sxs-lookup"><span data-stu-id="77ceb-105">DESCRIPTION</span></span>
<span data-ttu-id="77ceb-106">이 Set-AzIntegrationAccountGeneratedIcn cmdlet은 ICN(교환 컨트롤 번호)을 받은 기존 통합 계정을 업데이트하고 받은 교환 컨트롤 번호를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="77ceb-107">이 cmdlet을 사용하여 교환 컨트롤 번호의 메시지 처리 상태를 받은 통합 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="77ceb-108">통합 계정 이름, 리소스 그룹 이름, 규약 이름, 컨트롤 번호 값 및 메시지 처리 상태를 지정하여 통합 계정 수신 교환 컨트롤 번호를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="77ceb-109">이 명령을 사용하여 받은 새 통합 계정 교환 컨트롤 번호를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="77ceb-110">동적 매개 변수를 사용하거나 명령에 입력하거나 하이픈 기호(-)를 입력하여 매개 변수 이름을 나타내고 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="77ceb-111">필수 템플릿 매개 변수가 누락된 경우 cmdlet에 값을 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="77ceb-112">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="77ceb-113">"-AgreementType" 매개 변수를 제공하여 X12 또는 Edifact 컨트롤 번호가 반환될지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="77ceb-114">예제</span><span class="sxs-lookup"><span data-stu-id="77ceb-114">EXAMPLES</span></span>

### <span data-ttu-id="77ceb-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="77ceb-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="77ceb-116">이 명령은 특정 통합 계정 계약에 대한 X12 교환 제어 번호를 받은 통합 계정과 메시지 처리 상태가 실패한 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="77ceb-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="77ceb-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="77ceb-118">이 명령은 특정 통합 계정 계약에 대한 Edifact 교환 컨트롤 번호를 받은 통합 계정과 메시지 처리 상태가 실패한 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="77ceb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77ceb-119">PARAMETERS</span></span>

### <span data-ttu-id="77ceb-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="77ceb-120">-AgreementName</span></span>
<span data-ttu-id="77ceb-121">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="77ceb-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="77ceb-122">-AgreementType</span></span>
<span data-ttu-id="77ceb-123">통합 계정 계약 유형(X12 또는 Edifact)</span><span class="sxs-lookup"><span data-stu-id="77ceb-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="77ceb-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="77ceb-124">-ControlNumberValue</span></span>
<span data-ttu-id="77ceb-125">통합 계정 컨트롤 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="77ceb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ceb-126">-DefaultProfile</span></span>
<span data-ttu-id="77ceb-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="77ceb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77ceb-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="77ceb-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="77ceb-129">받은 메시지 처리 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ceb-130">-Name</span><span class="sxs-lookup"><span data-stu-id="77ceb-130">-Name</span></span>
<span data-ttu-id="77ceb-131">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-131">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ceb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ceb-132">-ResourceGroupName</span></span>
<span data-ttu-id="77ceb-133">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="77ceb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77ceb-134">-Confirm</span></span>
<span data-ttu-id="77ceb-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ceb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ceb-136">-WhatIf</span></span>
<span data-ttu-id="77ceb-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="77ceb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77ceb-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ceb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ceb-139">CommonParameters</span></span>
<span data-ttu-id="77ceb-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77ceb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ceb-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="77ceb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ceb-142">입력</span><span class="sxs-lookup"><span data-stu-id="77ceb-142">INPUTS</span></span>

### <span data-ttu-id="77ceb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="77ceb-143">System.String</span></span>

## <span data-ttu-id="77ceb-144">출력</span><span class="sxs-lookup"><span data-stu-id="77ceb-144">OUTPUTS</span></span>

### <span data-ttu-id="77ceb-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="77ceb-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="77ceb-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77ceb-146">NOTES</span></span>

## <span data-ttu-id="77ceb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77ceb-147">RELATED LINKS</span></span>

<span data-ttu-id="77ceb-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="77ceb-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
