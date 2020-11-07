---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 10cd1993acccf45e39a1b192f44b715b06f6d1d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689517"
---
# <span data-ttu-id="034d0-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="034d0-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="034d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034d0-102">SYNOPSIS</span></span>
<span data-ttu-id="034d0-103">통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="034d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="034d0-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="034d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="034d0-105">DESCRIPTION</span></span>
<span data-ttu-id="034d0-106">**새 AzIntegrationAccountAgreement** cmdlet은 통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="034d0-107">이 cmdlet은 통합 계정 계약을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="034d0-108">통합 계정 이름, 리소스 그룹 이름, 규약 이름, 유형, 파트너 이름, 파트너 한정자 및 규약 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="034d0-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="034d0-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="034d0-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="034d0-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="034d0-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="034d0-114">예제의</span><span class="sxs-lookup"><span data-stu-id="034d0-114">EXAMPLES</span></span>

### <span data-ttu-id="034d0-115">예제 1: 통합 계정 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="034d0-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="034d0-116">이 명령은 지정 된 Azure 리소스 그룹에 통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="034d0-117">변수</span><span class="sxs-lookup"><span data-stu-id="034d0-117">PARAMETERS</span></span>

### <span data-ttu-id="034d0-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="034d0-118">-AgreementContent</span></span>
<span data-ttu-id="034d0-119">규약에 대 한 규약 콘텐츠를 JSON (JavaScript 개체 표시법) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="034d0-120">이 매개 변수 또는 *AgreementContentFilePath* 매개 변수 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="034d0-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="034d0-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="034d0-122">규약에 대 한 규약 콘텐츠의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="034d0-123">이 매개 변수 또는 *AgreementContent* 매개 변수 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="034d0-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="034d0-124">-AgreementName</span></span>
<span data-ttu-id="034d0-125">통합 계정 계약의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="034d0-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="034d0-126">-AgreementType</span></span>
<span data-ttu-id="034d0-127">통합 계정 규약 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="034d0-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="034d0-129">X12</span><span class="sxs-lookup"><span data-stu-id="034d0-129">X12</span></span> 
- <span data-ttu-id="034d0-130">AS2</span><span class="sxs-lookup"><span data-stu-id="034d0-130">AS2</span></span>
- <span data-ttu-id="034d0-131">인</span><span class="sxs-lookup"><span data-stu-id="034d0-131">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034d0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034d0-132">-DefaultProfile</span></span>
<span data-ttu-id="034d0-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="034d0-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="034d0-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="034d0-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="034d0-135">게스트 파트너에 대 한 이름 비즈니스 id 한정자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="034d0-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="034d0-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="034d0-137">통합 계정 계약 게스트 id 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="034d0-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="034d0-138">-GuestPartner</span></span>
<span data-ttu-id="034d0-139">게스트 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="034d0-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="034d0-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="034d0-141">호스트 파트너에 대 한 이름 비즈니스 id 한정자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="034d0-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="034d0-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="034d0-143">통합 계정 계약 호스트 id 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="034d0-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="034d0-144">-HostPartner</span></span>
<span data-ttu-id="034d0-145">호스트 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="034d0-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="034d0-146">-Metadata</span></span>
<span data-ttu-id="034d0-147">규약에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034d0-148">-이름</span><span class="sxs-lookup"><span data-stu-id="034d0-148">-Name</span></span>
<span data-ttu-id="034d0-149">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-149">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034d0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034d0-150">-ResourceGroupName</span></span>
<span data-ttu-id="034d0-151">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="034d0-152">-확인</span><span class="sxs-lookup"><span data-stu-id="034d0-152">-Confirm</span></span>
<span data-ttu-id="034d0-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034d0-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034d0-154">-WhatIf</span></span>
<span data-ttu-id="034d0-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034d0-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034d0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034d0-157">CommonParameters</span></span>
<span data-ttu-id="034d0-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="034d0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034d0-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034d0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034d0-160">입력</span><span class="sxs-lookup"><span data-stu-id="034d0-160">INPUTS</span></span>

### <span data-ttu-id="034d0-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="034d0-161">System.String</span></span>

## <span data-ttu-id="034d0-162">출력</span><span class="sxs-lookup"><span data-stu-id="034d0-162">OUTPUTS</span></span>

### <span data-ttu-id="034d0-163">IntegrationAccountAgreement를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="034d0-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="034d0-164">상속자</span><span class="sxs-lookup"><span data-stu-id="034d0-164">NOTES</span></span>

## <span data-ttu-id="034d0-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="034d0-165">RELATED LINKS</span></span>

[<span data-ttu-id="034d0-166">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="034d0-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="034d0-167">제거-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="034d0-167">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="034d0-168">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="034d0-168">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


