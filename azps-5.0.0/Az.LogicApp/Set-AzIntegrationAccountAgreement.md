---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218953"
---
# <span data-ttu-id="29019-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="29019-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="29019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29019-102">SYNOPSIS</span></span>
<span data-ttu-id="29019-103">통합 계정 계약을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="29019-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29019-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29019-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29019-105">DESCRIPTION</span></span>
<span data-ttu-id="29019-106">**Set-AzIntegrationAccountAgreement** cmdlet은 통합 계정 계약을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="29019-107">이 cmdlet은 통합 계정 계약을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="29019-108">통합 계정 이름, 리소스 그룹 이름 및 규약 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="29019-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="29019-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="29019-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="29019-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="29019-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="29019-114">예제의</span><span class="sxs-lookup"><span data-stu-id="29019-114">EXAMPLES</span></span>

### <span data-ttu-id="29019-115">예제 1: 통합 계정 계약 업데이트</span><span class="sxs-lookup"><span data-stu-id="29019-115">Example 1: Update an integration account agreement</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="29019-116">이 명령은 지정 된 Azure 리소스 그룹의 통합 계정 계약을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="29019-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="29019-117">Example 2</span></span>

<span data-ttu-id="29019-118">통합 계정 계약을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="29019-119">생성</span><span class="sxs-lookup"><span data-stu-id="29019-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="29019-120">변수</span><span class="sxs-lookup"><span data-stu-id="29019-120">PARAMETERS</span></span>

### <span data-ttu-id="29019-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="29019-121">-AgreementContent</span></span>
<span data-ttu-id="29019-122">규약에 대 한 규약 콘텐츠를 JSON (JavaScript 개체 표시법) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="29019-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="29019-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="29019-124">규약에 대 한 규약 콘텐츠의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="29019-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="29019-125">-AgreementName</span></span>
<span data-ttu-id="29019-126">통합 계정 계약의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="29019-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="29019-127">-AgreementType</span></span>
<span data-ttu-id="29019-128">통합 계정 규약 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="29019-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="29019-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="29019-130">X12</span><span class="sxs-lookup"><span data-stu-id="29019-130">X12</span></span> 
- <span data-ttu-id="29019-131">AS2</span><span class="sxs-lookup"><span data-stu-id="29019-131">AS2</span></span>
- <span data-ttu-id="29019-132">인</span><span class="sxs-lookup"><span data-stu-id="29019-132">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29019-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29019-133">-DefaultProfile</span></span>
<span data-ttu-id="29019-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="29019-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29019-135">-Force</span><span class="sxs-lookup"><span data-stu-id="29019-135">-Force</span></span>
<span data-ttu-id="29019-136">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29019-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="29019-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="29019-138">게스트 파트너에 대 한 이름 비즈니스 id 한정자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="29019-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="29019-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="29019-140">통합 계정 계약 게스트 id 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="29019-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="29019-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="29019-141">-GuestPartner</span></span>
<span data-ttu-id="29019-142">게스트 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="29019-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="29019-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="29019-144">호스트 파트너에 대 한 이름 비즈니스 id 한정자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="29019-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="29019-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="29019-146">통합 계정 계약 호스트 id 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="29019-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="29019-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="29019-147">-HostPartner</span></span>
<span data-ttu-id="29019-148">호스트 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="29019-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="29019-149">-Metadata</span></span>
<span data-ttu-id="29019-150">규약에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="29019-151">-이름</span><span class="sxs-lookup"><span data-stu-id="29019-151">-Name</span></span>
<span data-ttu-id="29019-152">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="29019-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29019-153">-ResourceGroupName</span></span>
<span data-ttu-id="29019-154">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="29019-155">-확인</span><span class="sxs-lookup"><span data-stu-id="29019-155">-Confirm</span></span>
<span data-ttu-id="29019-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29019-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29019-157">-WhatIf</span></span>
<span data-ttu-id="29019-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29019-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29019-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29019-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29019-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29019-160">CommonParameters</span></span>
<span data-ttu-id="29019-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29019-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29019-162">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29019-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29019-163">입력</span><span class="sxs-lookup"><span data-stu-id="29019-163">INPUTS</span></span>

### <span data-ttu-id="29019-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="29019-164">System.String</span></span>

## <span data-ttu-id="29019-165">출력</span><span class="sxs-lookup"><span data-stu-id="29019-165">OUTPUTS</span></span>

### <span data-ttu-id="29019-166">IntegrationAccountAgreement를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="29019-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="29019-167">상속자</span><span class="sxs-lookup"><span data-stu-id="29019-167">NOTES</span></span>

## <span data-ttu-id="29019-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29019-168">RELATED LINKS</span></span>

[<span data-ttu-id="29019-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="29019-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="29019-170">새로운 AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="29019-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="29019-171">제거-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="29019-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


