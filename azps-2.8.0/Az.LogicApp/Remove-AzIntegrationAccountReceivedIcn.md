---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 416a5991be227364e4374d3e4c0e64caa3095b9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689491"
---
# <span data-ttu-id="82967-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="82967-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="82967-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82967-102">SYNOPSIS</span></span>
<span data-ttu-id="82967-103">이 cmdlet은 계약 및 컨트롤 번호 값에 따라 수신 되는 특정 교환 컨트롤 번호를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="82967-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82967-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82967-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82967-105">DESCRIPTION</span></span>
<span data-ttu-id="82967-106">이 cmdlet은 통합 계정에서 수신 된 교환 컨트롤 번호를 제거 하 여 중복 되는 번호 검색을 사용 하는 경우 해당 메시지에 대 한 다시 B2B 커넥터를 처리할 수 있도록 재난 복구 시나리오에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82967-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="82967-107">가끔 받은 교환 제어 번호는 재해가 발생 하기 전과 B2B 커넥터가 교환에 오류가 발생 하기 전에 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82967-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="82967-108">그러한 경우에는 페이로드를 수정한 후 복구 사이트에서 다시 동일한 교환 작업을 처리 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82967-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="82967-109">"-AgreementType" 매개 변수를 입력 하 여 X12 또는 Edifact 컨트롤 번호를 반환할지 여부를 지정 하십시오.</span><span class="sxs-lookup"><span data-stu-id="82967-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="82967-110">예제의</span><span class="sxs-lookup"><span data-stu-id="82967-110">EXAMPLES</span></span>

### <span data-ttu-id="82967-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="82967-111">Example 1</span></span>
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

<span data-ttu-id="82967-112">받은 X12 교환 컨트롤 번호를 가져오려고 시도 합니다. 유효한 형식이 아닌 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="82967-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="82967-113">수신 된 X12 교환 컨트롤 번호를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="82967-114">수신 된 X12 교환 컨트롤 번호가 제거 된 후 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="82967-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="82967-115">Example 2</span></span>
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

<span data-ttu-id="82967-116">받은 Edifact 교환 컨트롤 번호를 가져오려고 시도 합니다. 유효한 형식이 아닌 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="82967-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="82967-117">받은 Edifact 교환 컨트롤 번호를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="82967-118">받은 Edifact 교환 컨트롤 번호가 제거 된 후 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="82967-119">변수</span><span class="sxs-lookup"><span data-stu-id="82967-119">PARAMETERS</span></span>

### <span data-ttu-id="82967-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="82967-120">-AgreementName</span></span>
<span data-ttu-id="82967-121">통합 계정 규약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82967-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="82967-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="82967-122">-AgreementType</span></span>
<span data-ttu-id="82967-123">통합 계정 규약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="82967-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="82967-124">-Control번호 값</span><span class="sxs-lookup"><span data-stu-id="82967-124">-ControlNumberValue</span></span>
<span data-ttu-id="82967-125">통합 계정 컨트롤 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="82967-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="82967-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82967-126">-DefaultProfile</span></span>
<span data-ttu-id="82967-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="82967-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82967-128">-이름</span><span class="sxs-lookup"><span data-stu-id="82967-128">-Name</span></span>
<span data-ttu-id="82967-129">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82967-129">The integration account name.</span></span>

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

### <span data-ttu-id="82967-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82967-130">-ResourceGroupName</span></span>
<span data-ttu-id="82967-131">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82967-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="82967-132">-확인</span><span class="sxs-lookup"><span data-stu-id="82967-132">-Confirm</span></span>
<span data-ttu-id="82967-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82967-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82967-134">-WhatIf</span></span>
<span data-ttu-id="82967-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82967-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82967-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82967-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82967-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82967-137">CommonParameters</span></span>
<span data-ttu-id="82967-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82967-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82967-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82967-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82967-140">입력</span><span class="sxs-lookup"><span data-stu-id="82967-140">INPUTS</span></span>

### <span data-ttu-id="82967-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82967-141">System.String</span></span>

## <span data-ttu-id="82967-142">출력</span><span class="sxs-lookup"><span data-stu-id="82967-142">OUTPUTS</span></span>

### <span data-ttu-id="82967-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="82967-143">System.Void</span></span>

## <span data-ttu-id="82967-144">상속자</span><span class="sxs-lookup"><span data-stu-id="82967-144">NOTES</span></span>

## <span data-ttu-id="82967-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82967-145">RELATED LINKS</span></span>

<span data-ttu-id="82967-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="82967-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

