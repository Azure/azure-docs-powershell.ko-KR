---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878233"
---
# <span data-ttu-id="5edf9-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="5edf9-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="5edf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5edf9-102">SYNOPSIS</span></span>
<span data-ttu-id="5edf9-103">이 cmdlet은 계약 당 생성 된 교환 컨트롤 수의 현재 값을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="5edf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5edf9-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5edf9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5edf9-105">DESCRIPTION</span></span>
<span data-ttu-id="5edf9-106">이 cmdlet은 Set-AzIntegrationAccountGeneratedIcn를 사용 하 여 증가 하는 값을 기록 하기 위해 생성 된 교환 컨트롤 번호의 현재 값을 검색 하는 재해 복구 시나리오에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="5edf9-107">활성 지역에 재해가 발생 했을 때 아직 수동 지역으로 복제할 수 없는 숫자의 경우 교환 제어 번호가 중복 되는 것을 방지 하기 위해 늘려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="5edf9-108">"-AgreementType" 매개 변수를 입력 하 여 X12 또는 Edifact 컨트롤 번호를 반환할지 여부를 지정 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5edf9-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="5edf9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5edf9-109">EXAMPLES</span></span>

### <span data-ttu-id="5edf9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5edf9-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="5edf9-111">이 명령은 규약 이름을 기준으로 통합 계정 생성 X12 교환 컨트롤 번호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="5edf9-112">지정 된 규약이 "X12" 유형 인지 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="5edf9-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="5edf9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5edf9-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="5edf9-114">이 명령은 규약 이름을 기준으로 통합 계정에서 생성 된 Edifact 교환 컨트롤 번호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="5edf9-115">지정 된 규약이 "Edifact" 유형 인지 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="5edf9-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="5edf9-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="5edf9-116">Example 3</span></span>
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

<span data-ttu-id="5edf9-117">이 명령은 생성 된 모든 X12 교환 컨트롤 번호를 통합 계정 이름으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="5edf9-118">변수</span><span class="sxs-lookup"><span data-stu-id="5edf9-118">PARAMETERS</span></span>

### <span data-ttu-id="5edf9-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="5edf9-119">-AgreementName</span></span>
<span data-ttu-id="5edf9-120">통합 계정 규약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="5edf9-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="5edf9-121">-AgreementType</span></span>
<span data-ttu-id="5edf9-122">통합 계정 규약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="5edf9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edf9-123">-DefaultProfile</span></span>
<span data-ttu-id="5edf9-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5edf9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5edf9-125">-이름</span><span class="sxs-lookup"><span data-stu-id="5edf9-125">-Name</span></span>
<span data-ttu-id="5edf9-126">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-126">The integration account name.</span></span>

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

### <span data-ttu-id="5edf9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5edf9-127">-ResourceGroupName</span></span>
<span data-ttu-id="5edf9-128">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="5edf9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edf9-129">CommonParameters</span></span>
<span data-ttu-id="5edf9-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edf9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edf9-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edf9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edf9-132">입력</span><span class="sxs-lookup"><span data-stu-id="5edf9-132">INPUTS</span></span>

### <span data-ttu-id="5edf9-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5edf9-133">System.String</span></span>

## <span data-ttu-id="5edf9-134">출력</span><span class="sxs-lookup"><span data-stu-id="5edf9-134">OUTPUTS</span></span>

### <span data-ttu-id="5edf9-135">LogicApp. IntegrationAccountControlNumber. 유틸리티</span><span class="sxs-lookup"><span data-stu-id="5edf9-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="5edf9-136">상속자</span><span class="sxs-lookup"><span data-stu-id="5edf9-136">NOTES</span></span>

## <span data-ttu-id="5edf9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5edf9-137">RELATED LINKS</span></span>

[<span data-ttu-id="5edf9-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="5edf9-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

