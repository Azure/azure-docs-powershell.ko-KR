---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4dea211f2a09823161c1c6551b1fa00ab018a855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689473"
---
# <span data-ttu-id="67142-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="67142-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="67142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67142-102">SYNOPSIS</span></span>
<span data-ttu-id="67142-103">Azure 리소스 그룹에서 통합 계정 생성 된 ICN (교환 컨트롤 번호)을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="67142-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67142-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67142-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67142-105">DESCRIPTION</span></span>
<span data-ttu-id="67142-106">Set-AzIntegrationAccountGeneratedIcn cmdlet은 ICN (교환 제어 번호)이 생성 된 기존 통합 계정을 업데이트 하 고 통합 계정 생성 교환 컨트롤 번호를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="67142-107">이 cmdlet을 사용 하 여 통합 계정 생성 된 교환 컨트롤 번호를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="67142-108">통합 계정 이름, 리소스 그룹 이름 및 규약 이름을 지정 하 여 통합 계정 생성 된 교환 컨트롤 번호를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67142-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="67142-109">이 명령으로 새 통합 계정 생성 된 교환 컨트롤 번호를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="67142-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="67142-110">동적 매개 변수를 사용 하려면 명령에 입력 하거나 하이픈 기호 (-)를 입력 하 여 매개 변수 이름을 나타내고 TAB 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="67142-111">필수 템플릿 매개 변수를 놓친 경우 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="67142-112">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="67142-113">"-AgreementType" 매개 변수를 입력 하 여 X12 또는 Edifact 컨트롤 번호를 반환할지 여부를 지정 하십시오.</span><span class="sxs-lookup"><span data-stu-id="67142-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="67142-114">예제의</span><span class="sxs-lookup"><span data-stu-id="67142-114">EXAMPLES</span></span>

### <span data-ttu-id="67142-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="67142-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="67142-116">이 명령은 특정 통합 계정 규약에 대해 통합 계정 생성 X12 교환 컨트롤 번호를 가져오고 해당 값을 100으로 증가 시킨 다음 업데이트 된 값을 다시 씁니다.</span><span class="sxs-lookup"><span data-stu-id="67142-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="67142-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="67142-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="67142-118">이 명령은 특정 통합 계정 계약에 대해 생성 된 통합 계정 EdifactIntegrationAccountAgreement 교환 컨트롤 번호를 가져와 100으로 해당 값을 늘리고 업데이트 된 값을 다시 씁니다.</span><span class="sxs-lookup"><span data-stu-id="67142-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="67142-119">변수</span><span class="sxs-lookup"><span data-stu-id="67142-119">PARAMETERS</span></span>

### <span data-ttu-id="67142-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="67142-120">-AgreementName</span></span>
<span data-ttu-id="67142-121">통합 계정 규약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67142-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="67142-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="67142-122">-AgreementType</span></span>
<span data-ttu-id="67142-123">통합 계정 규약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="67142-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="67142-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="67142-124">-ControlNumber</span></span>
<span data-ttu-id="67142-125">생성 된 컨트롤 번호 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="67142-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="67142-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67142-126">-DefaultProfile</span></span>
<span data-ttu-id="67142-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67142-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67142-128">-이름</span><span class="sxs-lookup"><span data-stu-id="67142-128">-Name</span></span>
<span data-ttu-id="67142-129">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67142-129">The integration account name.</span></span>

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

### <span data-ttu-id="67142-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67142-130">-ResourceGroupName</span></span>
<span data-ttu-id="67142-131">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67142-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="67142-132">-확인</span><span class="sxs-lookup"><span data-stu-id="67142-132">-Confirm</span></span>
<span data-ttu-id="67142-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67142-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67142-134">-WhatIf</span></span>
<span data-ttu-id="67142-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67142-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67142-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67142-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67142-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67142-137">CommonParameters</span></span>
<span data-ttu-id="67142-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67142-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67142-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67142-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67142-140">입력</span><span class="sxs-lookup"><span data-stu-id="67142-140">INPUTS</span></span>

### <span data-ttu-id="67142-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67142-141">System.String</span></span>

## <span data-ttu-id="67142-142">출력</span><span class="sxs-lookup"><span data-stu-id="67142-142">OUTPUTS</span></span>

### <span data-ttu-id="67142-143">LogicApp. IntegrationAccountControlNumber. 유틸리티</span><span class="sxs-lookup"><span data-stu-id="67142-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="67142-144">상속자</span><span class="sxs-lookup"><span data-stu-id="67142-144">NOTES</span></span>

## <span data-ttu-id="67142-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67142-145">RELATED LINKS</span></span>

[<span data-ttu-id="67142-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="67142-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

