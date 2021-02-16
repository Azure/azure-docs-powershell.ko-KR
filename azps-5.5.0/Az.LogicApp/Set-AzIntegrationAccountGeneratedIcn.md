---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187569"
---
# <span data-ttu-id="47586-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="47586-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="47586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47586-102">SYNOPSIS</span></span>
<span data-ttu-id="47586-103">Azure 리소스 그룹에서 통합 계정에서 생성된 ICN(교환 제어 번호)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="47586-104">구문</span><span class="sxs-lookup"><span data-stu-id="47586-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47586-105">설명</span><span class="sxs-lookup"><span data-stu-id="47586-105">DESCRIPTION</span></span>
<span data-ttu-id="47586-106">이 Set-AzIntegrationAccountGeneratedIcn cmdlet은 기존 통합 계정 생성 교환 제어 번호(ICN)를 업데이트하고 통합 계정에서 생성된 교환 컨트롤 번호를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="47586-107">이 cmdlet을 사용하여 통합 계정에서 생성된 교환 컨트롤 번호를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="47586-108">통합 계정 이름, 리소스 그룹 이름 및 규약 이름을 지정하여 통합 계정에서 생성된 교환 제어 번호를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47586-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="47586-109">이 명령을 사용하여 생성된 교환 컨트롤 번호를 새 통합 계정으로 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47586-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="47586-110">동적 매개 변수를 사용하거나 명령에 입력하거나 하이픈 기호(-)를 입력하여 매개 변수 이름을 나타내고 TAB 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="47586-111">필수 템플릿 매개 변수가 누락된 경우 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="47586-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="47586-112">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="47586-113">"-AgreementType" 매개 변수를 제공하여 X12 또는 Edifact 컨트롤 번호를 반환할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="47586-114">예제</span><span class="sxs-lookup"><span data-stu-id="47586-114">EXAMPLES</span></span>

### <span data-ttu-id="47586-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="47586-115">Example 1</span></span>
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

<span data-ttu-id="47586-116">이 명령은 특정 통합 계정 계약에 대해 생성된 통합 계정 생성 X12 교환 컨트롤 번호를 얻게 하여 해당 값을 100으로 늘렸다가 업데이트된 값을 다시 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="47586-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="47586-117">Example 2</span></span>
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

<span data-ttu-id="47586-118">이 명령은 특정 통합 계정 계약에 대해 생성된 통합 계정 생성 EdifactIntegrationAccountAgreement 교환 컨트롤 번호를 구하고 해당 값을 100으로 늘린 다음 업데이트된 값을 다시 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="47586-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47586-119">PARAMETERS</span></span>

### <span data-ttu-id="47586-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="47586-120">-AgreementName</span></span>
<span data-ttu-id="47586-121">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47586-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="47586-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="47586-122">-AgreementType</span></span>
<span data-ttu-id="47586-123">통합 계정 계약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="47586-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="47586-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="47586-124">-ControlNumber</span></span>
<span data-ttu-id="47586-125">생성된 컨트롤 번호 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="47586-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="47586-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47586-126">-DefaultProfile</span></span>
<span data-ttu-id="47586-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="47586-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47586-128">-Name</span><span class="sxs-lookup"><span data-stu-id="47586-128">-Name</span></span>
<span data-ttu-id="47586-129">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47586-129">The integration account name.</span></span>

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

### <span data-ttu-id="47586-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47586-130">-ResourceGroupName</span></span>
<span data-ttu-id="47586-131">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47586-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="47586-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47586-132">-Confirm</span></span>
<span data-ttu-id="47586-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47586-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47586-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47586-134">-WhatIf</span></span>
<span data-ttu-id="47586-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="47586-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47586-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47586-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47586-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47586-137">CommonParameters</span></span>
<span data-ttu-id="47586-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47586-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47586-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="47586-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47586-140">입력</span><span class="sxs-lookup"><span data-stu-id="47586-140">INPUTS</span></span>

### <span data-ttu-id="47586-141">System.String</span><span class="sxs-lookup"><span data-stu-id="47586-141">System.String</span></span>

## <span data-ttu-id="47586-142">출력</span><span class="sxs-lookup"><span data-stu-id="47586-142">OUTPUTS</span></span>

### <span data-ttu-id="47586-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="47586-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="47586-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47586-144">NOTES</span></span>

## <span data-ttu-id="47586-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47586-145">RELATED LINKS</span></span>

[<span data-ttu-id="47586-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="47586-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

