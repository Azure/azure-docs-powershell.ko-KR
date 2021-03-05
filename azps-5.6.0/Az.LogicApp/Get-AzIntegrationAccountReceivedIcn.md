---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: df7266548b616615fa45131c21f40622894ffe9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960576"
---
# <span data-ttu-id="fb7cb-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="fb7cb-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="fb7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7cb-103">이 cmdlet은 계약 및 제어 번호 값당 받은 특정 교환 제어 번호를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="fb7cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb7cb-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb7cb-105">설명</span><span class="sxs-lookup"><span data-stu-id="fb7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="fb7cb-106">이 cmdlet은 재해 복구 시나리오에서 수신된 교환 제어 번호의 유효성을 검사하고, 선택적으로 Remove-AzIntegrationAccountReceivedIcn을 사용하여 해당 엔터티를 제거하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="fb7cb-107">반환할 X12 또는 Edifact 제어 번호 여부를 지정하기 위해 "-AgreementType" 매개 변수를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="fb7cb-108">예제</span><span class="sxs-lookup"><span data-stu-id="fb7cb-108">EXAMPLES</span></span>

### <span data-ttu-id="fb7cb-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb7cb-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="fb7cb-110">이 명령은 계약 이름 및 제어 번호 값에 따라 X12 통합 계정이 받은 교환 제어 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="fb7cb-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="fb7cb-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="fb7cb-112">이 명령은 계약 이름 및 제어 번호 값에 따라 Edifact 통합 계정이 받은 교환 제어 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="fb7cb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fb7cb-113">PARAMETERS</span></span>

### <span data-ttu-id="fb7cb-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="fb7cb-114">-AgreementName</span></span>
<span data-ttu-id="fb7cb-115">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="fb7cb-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="fb7cb-116">-AgreementType</span></span>
<span data-ttu-id="fb7cb-117">통합 계정 계약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="fb7cb-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="fb7cb-118">-ControlNumberValue</span></span>
<span data-ttu-id="fb7cb-119">통합 계정 제어 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="fb7cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7cb-120">-DefaultProfile</span></span>
<span data-ttu-id="fb7cb-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb7cb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb7cb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb7cb-122">-Name</span></span>
<span data-ttu-id="fb7cb-123">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-123">The integration account name.</span></span>

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

### <span data-ttu-id="fb7cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb7cb-125">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="fb7cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7cb-126">CommonParameters</span></span>
<span data-ttu-id="fb7cb-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7cb-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7cb-129">입력</span><span class="sxs-lookup"><span data-stu-id="fb7cb-129">INPUTS</span></span>

### <span data-ttu-id="fb7cb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fb7cb-130">System.String</span></span>

## <span data-ttu-id="fb7cb-131">출력</span><span class="sxs-lookup"><span data-stu-id="fb7cb-131">OUTPUTS</span></span>

### <span data-ttu-id="fb7cb-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="fb7cb-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="fb7cb-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb7cb-133">NOTES</span></span>

## <span data-ttu-id="fb7cb-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb7cb-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb7cb-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="fb7cb-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="fb7cb-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="fb7cb-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
