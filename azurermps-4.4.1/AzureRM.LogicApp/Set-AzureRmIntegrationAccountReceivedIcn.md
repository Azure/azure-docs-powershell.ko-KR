---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: fbbc071b9c83336a1835f1495d171f7a2414199a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703703"
---
# <span data-ttu-id="c22d0-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c22d0-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c22d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c22d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c22d0-103">Azure 리소스 그룹에서 통합 계정이 받은 ICN (교환 컨트롤 번호)을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c22d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c22d0-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c22d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c22d0-105">DESCRIPTION</span></span>
<span data-ttu-id="c22d0-106">Set-AzureRmIntegrationAccountGeneratedIcn cmdlet은 ICN (교환 컨트롤 번호)을 받았으며 통합 계정에서 받은 교환 컨트롤 번호를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="c22d0-107">이 cmdlet을 사용 하 여 통합 계정에서 교환 컨트롤 번호를 받은 메시지 처리 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="c22d0-108">통합 계정 이름, 리소스 그룹 이름, 규약 이름, 컨트롤 번호 값, 메시지 처리 상태를 지정 하 여 계정에 교환 제어 번호를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="c22d0-109">이 명령을 사용 하 여 새 통합 계정을 만들 수 없습니다. 교환 컨트롤 번호를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="c22d0-110">동적 매개 변수를 사용 하려면 명령에 입력 하거나 하이픈 기호 (-)를 입력 하 여 매개 변수 이름을 나타내고 TAB 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c22d0-111">필수 템플릿 매개 변수를 놓친 경우 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="c22d0-112">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="c22d0-113">"-AgreementType" 매개 변수를 입력 하 여 X12 또는 Edifact 컨트롤 번호를 반환할지 여부를 지정 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c22d0-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c22d0-114">예제의</span><span class="sxs-lookup"><span data-stu-id="c22d0-114">EXAMPLES</span></span>

### <span data-ttu-id="c22d0-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="c22d0-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="c22d0-116">이 명령은 통합 계정이 업데이트 됨 특정 통합 계정 계약과 값에 대해 X12 교환 제어 번호를 수신 하 여 메시지 처리 상태가 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="c22d0-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="c22d0-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="c22d0-118">이 명령은 통합 계정이 업데이트 됨 지정한 통합 계정 계약 및 값에 대 한 Edifact 교환 컨트롤 번호 (메시지 처리 상태가 실패 함)가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="c22d0-119">변수</span><span class="sxs-lookup"><span data-stu-id="c22d0-119">PARAMETERS</span></span>

### <span data-ttu-id="c22d0-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c22d0-120">-AgreementName</span></span>
<span data-ttu-id="c22d0-121">통합 계정 규약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c22d0-122">-Control번호 값</span><span class="sxs-lookup"><span data-stu-id="c22d0-122">-ControlNumberValue</span></span>
<span data-ttu-id="c22d0-123">통합 계정 컨트롤 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-123">The integration account control number value.</span></span>

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

### <span data-ttu-id="c22d0-124">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="c22d0-124">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="c22d0-125">받은 메시지 처리 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-125">The received message processing status.</span></span>

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

### <span data-ttu-id="c22d0-126">-이름</span><span class="sxs-lookup"><span data-stu-id="c22d0-126">-Name</span></span>
<span data-ttu-id="c22d0-127">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-127">The integration account name.</span></span>

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

### <span data-ttu-id="c22d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="c22d0-129">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-129">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c22d0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="c22d0-130">-Confirm</span></span>
<span data-ttu-id="c22d0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c22d0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c22d0-132">-WhatIf</span></span>
<span data-ttu-id="c22d0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c22d0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c22d0-135">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="c22d0-135">-AgreementType</span></span>
<span data-ttu-id="c22d0-136">X12 또는 Edifact (통합 계정 계약 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-136">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22d0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22d0-137">-DefaultProfile</span></span>
<span data-ttu-id="c22d0-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c22d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22d0-139">CommonParameters</span></span>
<span data-ttu-id="c22d0-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22d0-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22d0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22d0-142">입력</span><span class="sxs-lookup"><span data-stu-id="c22d0-142">INPUTS</span></span>

### <span data-ttu-id="c22d0-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c22d0-143">System.String</span></span>

## <span data-ttu-id="c22d0-144">출력</span><span class="sxs-lookup"><span data-stu-id="c22d0-144">OUTPUTS</span></span>

### <span data-ttu-id="c22d0-145">LogicApp. IntegrationAccountControlNumber. 유틸리티</span><span class="sxs-lookup"><span data-stu-id="c22d0-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="c22d0-146">상속자</span><span class="sxs-lookup"><span data-stu-id="c22d0-146">NOTES</span></span>

## <span data-ttu-id="c22d0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c22d0-147">RELATED LINKS</span></span>

<span data-ttu-id="c22d0-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [제거-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="c22d0-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
