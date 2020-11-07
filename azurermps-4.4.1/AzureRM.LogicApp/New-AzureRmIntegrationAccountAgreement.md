---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: b95ab13e7ea35e1b41f449f461892e7ea324aa97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711884"
---
# <span data-ttu-id="c7aa7-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c7aa7-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="c7aa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c7aa7-103">통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7aa7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7aa7-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7aa7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="c7aa7-106">**새 AzureRmIntegrationAccountAgreement** cmdlet은 통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="c7aa7-107">이 cmdlet은 통합 계정 계약을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="c7aa7-108">통합 계정 이름, 리소스 그룹 이름, 규약 이름, 유형, 파트너 이름, 파트너 한정자 및 규약 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="c7aa7-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="c7aa7-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c7aa7-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c7aa7-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c7aa7-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c7aa7-114">예제의</span><span class="sxs-lookup"><span data-stu-id="c7aa7-114">EXAMPLES</span></span>

### <span data-ttu-id="c7aa7-115">예제 1: 통합 계정 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="c7aa7-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="c7aa7-116">이 명령은 지정 된 Azure 리소스 그룹에 통합 계정 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="c7aa7-117">변수</span><span class="sxs-lookup"><span data-stu-id="c7aa7-117">PARAMETERS</span></span>

### <span data-ttu-id="c7aa7-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="c7aa7-118">-AgreementContent</span></span>
<span data-ttu-id="c7aa7-119">규약에 대 한 규약 콘텐츠를 JSON (JavaScript 개체 표시법) 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="c7aa7-120">이 매개 변수 또는 *AgreementContentFilePath* 매개 변수 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="c7aa7-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="c7aa7-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="c7aa7-122">규약에 대 한 규약 콘텐츠의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="c7aa7-123">이 매개 변수 또는 *AgreementContent* 매개 변수 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="c7aa7-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c7aa7-124">-AgreementName</span></span>
<span data-ttu-id="c7aa7-125">통합 계정 계약의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="c7aa7-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="c7aa7-126">-AgreementType</span></span>
<span data-ttu-id="c7aa7-127">통합 계정 규약 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="c7aa7-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7aa7-129">X12</span><span class="sxs-lookup"><span data-stu-id="c7aa7-129">X12</span></span> 
- <span data-ttu-id="c7aa7-130">AS2</span><span class="sxs-lookup"><span data-stu-id="c7aa7-130">AS2</span></span>
- <span data-ttu-id="c7aa7-131">인</span><span class="sxs-lookup"><span data-stu-id="c7aa7-131">Edifact</span></span>

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

### <span data-ttu-id="c7aa7-132">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="c7aa7-132">-GuestIdentityQualifier</span></span>
<span data-ttu-id="c7aa7-133">게스트 파트너에 대 한 이름 비즈니스 id 한정자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-133">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="c7aa7-134">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="c7aa7-134">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="c7aa7-135">통합 계정 계약 게스트 id 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-135">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="c7aa7-136">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="c7aa7-136">-GuestPartner</span></span>
<span data-ttu-id="c7aa7-137">게스트 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-137">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="c7aa7-138">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="c7aa7-138">-HostIdentityQualifier</span></span>
<span data-ttu-id="c7aa7-139">호스트 파트너에 대 한 이름 비즈니스 id 한정자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-139">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="c7aa7-140">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="c7aa7-140">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="c7aa7-141">통합 계정 계약 호스트 id 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-141">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="c7aa7-142">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="c7aa7-142">-HostPartner</span></span>
<span data-ttu-id="c7aa7-143">호스트 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-143">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="c7aa7-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c7aa7-144">-Metadata</span></span>
<span data-ttu-id="c7aa7-145">규약에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-145">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="c7aa7-146">-이름</span><span class="sxs-lookup"><span data-stu-id="c7aa7-146">-Name</span></span>
<span data-ttu-id="c7aa7-147">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-147">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="c7aa7-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7aa7-148">-ResourceGroupName</span></span>
<span data-ttu-id="c7aa7-149">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-149">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c7aa7-150">-확인</span><span class="sxs-lookup"><span data-stu-id="c7aa7-150">-Confirm</span></span>
<span data-ttu-id="c7aa7-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7aa7-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7aa7-152">-WhatIf</span></span>
<span data-ttu-id="c7aa7-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7aa7-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7aa7-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7aa7-155">-DefaultProfile</span></span>
<span data-ttu-id="c7aa7-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7aa7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7aa7-157">CommonParameters</span></span>
<span data-ttu-id="c7aa7-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7aa7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7aa7-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7aa7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7aa7-160">입력</span><span class="sxs-lookup"><span data-stu-id="c7aa7-160">INPUTS</span></span>

## <span data-ttu-id="c7aa7-161">출력</span><span class="sxs-lookup"><span data-stu-id="c7aa7-161">OUTPUTS</span></span>

### <span data-ttu-id="c7aa7-162">IntegrationAccountAgreement를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="c7aa7-162">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="c7aa7-163">상속자</span><span class="sxs-lookup"><span data-stu-id="c7aa7-163">NOTES</span></span>

## <span data-ttu-id="c7aa7-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7aa7-164">RELATED LINKS</span></span>

[<span data-ttu-id="c7aa7-165">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c7aa7-165">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="c7aa7-166">제거-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c7aa7-166">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="c7aa7-167">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c7aa7-167">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


