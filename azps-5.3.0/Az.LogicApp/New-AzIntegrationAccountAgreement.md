---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495428"
---
# <span data-ttu-id="679ca-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="679ca-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="679ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679ca-102">SYNOPSIS</span></span>
<span data-ttu-id="679ca-103">통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="679ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="679ca-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679ca-105">설명</span><span class="sxs-lookup"><span data-stu-id="679ca-105">DESCRIPTION</span></span>
<span data-ttu-id="679ca-106">**New-AzIntegrationAccountAgreement** cmdlet은 통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="679ca-107">이 cmdlet은 통합 계정 계약을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="679ca-108">통합 계정 이름, 리소스 그룹 이름, 계약 이름, 유형, 파트너 이름, 파트너 지정자 및 계약 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="679ca-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="679ca-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="679ca-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="679ca-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="679ca-113">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="679ca-114">예제</span><span class="sxs-lookup"><span data-stu-id="679ca-114">EXAMPLES</span></span>

### <span data-ttu-id="679ca-115">예제 1: 통합 계정 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="679ca-115">Example 1: Create a integration account agreement</span></span>
```powershell
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

<span data-ttu-id="679ca-116">이 명령은 지정된 Azure 리소스 그룹에 통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="679ca-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="679ca-117">Example 2</span></span>

<span data-ttu-id="679ca-118">통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-118">Creates an integration account agreement.</span></span> <span data-ttu-id="679ca-119">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="679ca-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="679ca-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="679ca-120">PARAMETERS</span></span>

### <span data-ttu-id="679ca-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="679ca-121">-AgreementContent</span></span>
<span data-ttu-id="679ca-122">계약에 대한 계약 콘텐츠를 JSON(JavaScript Object Notation) 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="679ca-123">이 매개 변수 또는 *AgreementContentFilePath* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="679ca-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="679ca-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="679ca-125">계약에 대한 협정 콘텐츠의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="679ca-126">이 매개 변수 또는 *AgreementContent 매개 변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="679ca-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="679ca-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="679ca-127">-AgreementName</span></span>
<span data-ttu-id="679ca-128">통합 계정 계약의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="679ca-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="679ca-129">-AgreementType</span></span>
<span data-ttu-id="679ca-130">통합 계정 계약 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="679ca-131">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="679ca-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="679ca-132">X12</span><span class="sxs-lookup"><span data-stu-id="679ca-132">X12</span></span> 
- <span data-ttu-id="679ca-133">AS2</span><span class="sxs-lookup"><span data-stu-id="679ca-133">AS2</span></span>
- <span data-ttu-id="679ca-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="679ca-134">Edifact</span></span>

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

### <span data-ttu-id="679ca-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679ca-135">-DefaultProfile</span></span>
<span data-ttu-id="679ca-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="679ca-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="679ca-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="679ca-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="679ca-138">게스트 파트너에 대한 이름 비즈니스 ID 한정자 지정자입니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="679ca-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="679ca-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="679ca-140">통합 계정 계약 게스트 ID 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="679ca-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="679ca-141">-GuestPartner</span></span>
<span data-ttu-id="679ca-142">게스트 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="679ca-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="679ca-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="679ca-144">호스트 파트너에 대한 이름 비즈니스 ID 한정자 지정자입니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="679ca-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="679ca-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="679ca-146">통합 계정 계약 호스트 ID 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="679ca-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="679ca-147">-HostPartner</span></span>
<span data-ttu-id="679ca-148">호스트 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="679ca-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="679ca-149">-Metadata</span></span>
<span data-ttu-id="679ca-150">계약에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="679ca-151">-Name</span><span class="sxs-lookup"><span data-stu-id="679ca-151">-Name</span></span>
<span data-ttu-id="679ca-152">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="679ca-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679ca-153">-ResourceGroupName</span></span>
<span data-ttu-id="679ca-154">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="679ca-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="679ca-155">-Confirm</span></span>
<span data-ttu-id="679ca-156">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679ca-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679ca-157">-WhatIf</span></span>
<span data-ttu-id="679ca-158">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="679ca-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679ca-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679ca-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679ca-160">CommonParameters</span></span>
<span data-ttu-id="679ca-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="679ca-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679ca-162">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="679ca-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679ca-163">입력</span><span class="sxs-lookup"><span data-stu-id="679ca-163">INPUTS</span></span>

### <span data-ttu-id="679ca-164">System.String</span><span class="sxs-lookup"><span data-stu-id="679ca-164">System.String</span></span>

## <span data-ttu-id="679ca-165">출력</span><span class="sxs-lookup"><span data-stu-id="679ca-165">OUTPUTS</span></span>

### <span data-ttu-id="679ca-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="679ca-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="679ca-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="679ca-167">NOTES</span></span>

## <span data-ttu-id="679ca-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="679ca-168">RELATED LINKS</span></span>

[<span data-ttu-id="679ca-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="679ca-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="679ca-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="679ca-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="679ca-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="679ca-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


