---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048208"
---
# <span data-ttu-id="34bfb-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="34bfb-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="34bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="34bfb-103">이 cmdlet은 계약 및 컨트롤 번호 값에 따라 수신 된 특정 교환 컨트롤 번호를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="34bfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34bfb-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34bfb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="34bfb-106">이 cmdlet은 받은 교환 컨트롤 번호가 있는지 확인 하 고 필요에 따라 제거-AzIntegrationAccountReceivedIcn를 사용 하 여 해당 엔터티를 제거 하는 재해 복구 시나리오에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="34bfb-107">"-AgreementType" 매개 변수를 입력 하 여 X12 또는 Edifact 컨트롤 번호를 반환할지 여부를 지정 하십시오.</span><span class="sxs-lookup"><span data-stu-id="34bfb-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="34bfb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="34bfb-108">EXAMPLES</span></span>

### <span data-ttu-id="34bfb-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="34bfb-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="34bfb-110">이 명령은 X12 통합 계정에서 규약 이름 및 컨트롤 번호 값을 기준으로 교환 컨트롤 번호를 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="34bfb-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="34bfb-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="34bfb-112">이 명령은 Edifact 통합 계정에서 규약 이름 및 컨트롤 번호 값을 기준으로 교환 컨트롤 번호를 받음으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="34bfb-113">변수</span><span class="sxs-lookup"><span data-stu-id="34bfb-113">PARAMETERS</span></span>

### <span data-ttu-id="34bfb-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="34bfb-114">-AgreementName</span></span>
<span data-ttu-id="34bfb-115">통합 계정 규약 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="34bfb-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="34bfb-116">-AgreementType</span></span>
<span data-ttu-id="34bfb-117">통합 계정 규약 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="34bfb-118">-Control번호 값</span><span class="sxs-lookup"><span data-stu-id="34bfb-118">-ControlNumberValue</span></span>
<span data-ttu-id="34bfb-119">통합 계정 컨트롤 번호 값입니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="34bfb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bfb-120">-DefaultProfile</span></span>
<span data-ttu-id="34bfb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="34bfb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34bfb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="34bfb-122">-Name</span></span>
<span data-ttu-id="34bfb-123">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-123">The integration account name.</span></span>

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

### <span data-ttu-id="34bfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="34bfb-125">통합 계정 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="34bfb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bfb-126">CommonParameters</span></span>
<span data-ttu-id="34bfb-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34bfb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bfb-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34bfb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bfb-129">입력</span><span class="sxs-lookup"><span data-stu-id="34bfb-129">INPUTS</span></span>

### <span data-ttu-id="34bfb-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34bfb-130">System.String</span></span>

## <span data-ttu-id="34bfb-131">출력</span><span class="sxs-lookup"><span data-stu-id="34bfb-131">OUTPUTS</span></span>

### <span data-ttu-id="34bfb-132">LogicApp. IntegrationAccountControlNumber. 유틸리티</span><span class="sxs-lookup"><span data-stu-id="34bfb-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="34bfb-133">상속자</span><span class="sxs-lookup"><span data-stu-id="34bfb-133">NOTES</span></span>

## <span data-ttu-id="34bfb-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34bfb-134">RELATED LINKS</span></span>

[<span data-ttu-id="34bfb-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="34bfb-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="34bfb-136">제거-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="34bfb-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
