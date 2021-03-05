---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b6bf2c126a1009d824ab8bae1ea2e2031459d876
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960608"
---
# <span data-ttu-id="8261b-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8261b-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="8261b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8261b-102">SYNOPSIS</span></span>
<span data-ttu-id="8261b-103">이 cmdlet은 계약당 생성된 교환 제어 번호의 현재 값을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="8261b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8261b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8261b-105">설명</span><span class="sxs-lookup"><span data-stu-id="8261b-105">DESCRIPTION</span></span>
<span data-ttu-id="8261b-106">이 cmdlet은 재해 복구 시나리오에서 생성된 교환 제어 번호의 현재 값을 검색하여 Set-AzIntegrationAccountGeneratedIcn으로 증가된 값을 기록하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="8261b-107">활성 지역에서 재해가 발생하면 수동 지역에 복제할 수 없는 숫자에 대한 중복 교환 제어 번호를 피하기 위해 교환 제어 번호를 늘림해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="8261b-108">반환할 X12 또는 Edifact 제어 번호 여부를 지정하기 위해 "-AgreementType" 매개 변수를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="8261b-109">예제</span><span class="sxs-lookup"><span data-stu-id="8261b-109">EXAMPLES</span></span>

### <span data-ttu-id="8261b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8261b-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8261b-111">이 명령은 계약 이름에 따라 생성된 통합 계정 X12 교환 제어 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="8261b-112">지정된 계약이 "X12" 형식인지 확인하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="8261b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8261b-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8261b-114">이 명령은 Edifact에서 생성된 통합 계정 교환 제어 번호를 계약 이름에 따라 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="8261b-115">지정된 계약이 "Edifact" 형식인지 확인하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="8261b-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="8261b-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="8261b-117">이 명령은 통합 계정 이름으로 생성된 모든 X12 교환 제어 번호를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="8261b-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8261b-118">PARAMETERS</span></span>

### <span data-ttu-id="8261b-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="8261b-119">-AgreementName</span></span>
<span data-ttu-id="8261b-120">통합 계정 계약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8261b-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="8261b-121">-AgreementType</span></span>
<span data-ttu-id="8261b-122">통합 계정 계약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="8261b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8261b-123">-DefaultProfile</span></span>
<span data-ttu-id="8261b-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8261b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8261b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8261b-125">-Name</span></span>
<span data-ttu-id="8261b-126">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-126">The integration account name.</span></span>

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

### <span data-ttu-id="8261b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8261b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8261b-128">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="8261b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8261b-129">CommonParameters</span></span>
<span data-ttu-id="8261b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8261b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8261b-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8261b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8261b-132">입력</span><span class="sxs-lookup"><span data-stu-id="8261b-132">INPUTS</span></span>

### <span data-ttu-id="8261b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8261b-133">System.String</span></span>

## <span data-ttu-id="8261b-134">출력</span><span class="sxs-lookup"><span data-stu-id="8261b-134">OUTPUTS</span></span>

### <span data-ttu-id="8261b-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="8261b-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="8261b-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8261b-136">NOTES</span></span>

## <span data-ttu-id="8261b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8261b-137">RELATED LINKS</span></span>

[<span data-ttu-id="8261b-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8261b-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

