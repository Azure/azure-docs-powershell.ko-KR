---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4c91ced490226901a45e0eacb7caa204daa20558
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976811"
---
# <span data-ttu-id="6075c-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="6075c-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="6075c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6075c-102">SYNOPSIS</span></span>
<span data-ttu-id="6075c-103">Azure 리소스 그룹의 통합 계정 생성 교환 제어 번호(ICN)를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="6075c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6075c-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6075c-105">설명</span><span class="sxs-lookup"><span data-stu-id="6075c-105">DESCRIPTION</span></span>
<span data-ttu-id="6075c-106">Set-AzIntegrationAccountGeneratedIcn cmdlet은 ICN(기존 통합 계정 생성 교환 제어 번호)을 업데이트하고 통합 계정 생성 교환 제어 번호를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="6075c-107">이 cmdlet을 사용하여 통합 계정 생성 교환 제어 번호를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="6075c-108">통합 계정 이름, 리소스 그룹 이름 및 계약 이름을 지정하여 통합 계정 생성 교환 제어 번호를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="6075c-109">이 명령과 함께 생성된 새 통합 계정 교환 제어 번호를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="6075c-110">동적 매개 변수를 사용하기 위해 명령에 입력하거나 하이픈 기호(-)를 입력하여 매개 변수 이름을 나타내고 TAB 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6075c-111">필요한 템플릿 매개 변수가 누락된 경우 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="6075c-112">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6075c-113">반환할 X12 또는 Edifact 제어 번호 여부를 지정하기 위해 "-AgreementType" 매개 변수를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="6075c-114">예제</span><span class="sxs-lookup"><span data-stu-id="6075c-114">EXAMPLES</span></span>

### <span data-ttu-id="6075c-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="6075c-115">Example 1</span></span>
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

<span data-ttu-id="6075c-116">이 명령은 특정 통합 계정 계약에 대해 생성된 통합 계정 X12 교환 제어 번호를 얻게 하여 해당 값을 100으로 증가한 다음 업데이트된 값을 다시 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="6075c-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="6075c-117">Example 2</span></span>
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

<span data-ttu-id="6075c-118">이 명령은 특정 통합 계정 계약에 대한 통합 계정 생성 EdifactIntegrationAccountAgreement 교환 제어 번호를 얻게 하여 해당 값을 100으로 증가한 다음 업데이트된 값을 다시 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="6075c-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6075c-119">PARAMETERS</span></span>

### <span data-ttu-id="6075c-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6075c-120">-AgreementName</span></span>
<span data-ttu-id="6075c-121">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="6075c-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6075c-122">-AgreementType</span></span>
<span data-ttu-id="6075c-123">통합 계정 계약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="6075c-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="6075c-124">-ControlNumber</span></span>
<span data-ttu-id="6075c-125">생성된 컨트롤 번호 새 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="6075c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6075c-126">-DefaultProfile</span></span>
<span data-ttu-id="6075c-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6075c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6075c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6075c-128">-Name</span></span>
<span data-ttu-id="6075c-129">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-129">The integration account name.</span></span>

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

### <span data-ttu-id="6075c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6075c-130">-ResourceGroupName</span></span>
<span data-ttu-id="6075c-131">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="6075c-132">-확인</span><span class="sxs-lookup"><span data-stu-id="6075c-132">-Confirm</span></span>
<span data-ttu-id="6075c-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6075c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6075c-134">-WhatIf</span></span>
<span data-ttu-id="6075c-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6075c-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6075c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6075c-137">CommonParameters</span></span>
<span data-ttu-id="6075c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6075c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6075c-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6075c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6075c-140">입력</span><span class="sxs-lookup"><span data-stu-id="6075c-140">INPUTS</span></span>

### <span data-ttu-id="6075c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6075c-141">System.String</span></span>

## <span data-ttu-id="6075c-142">출력</span><span class="sxs-lookup"><span data-stu-id="6075c-142">OUTPUTS</span></span>

### <span data-ttu-id="6075c-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="6075c-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="6075c-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6075c-144">NOTES</span></span>

## <span data-ttu-id="6075c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6075c-145">RELATED LINKS</span></span>

[<span data-ttu-id="6075c-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="6075c-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

