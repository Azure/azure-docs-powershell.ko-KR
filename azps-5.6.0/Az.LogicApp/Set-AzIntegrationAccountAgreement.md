---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 6c7781f5617571003083328adfac8aa7b349841b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962939"
---
# <span data-ttu-id="cf9a4-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf9a4-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="cf9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9a4-103">통합 계정 계약을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="cf9a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf9a4-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf9a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="cf9a4-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9a4-106">**Set-AzIntegrationAccountAgreement** cmdlet은 통합 계정 계약을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="cf9a4-107">이 cmdlet은 통합 계정 계약을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="cf9a4-108">통합 계정 이름, 리소스 그룹 이름 및 계약 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="cf9a4-109">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="cf9a4-110">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cf9a4-111">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cf9a4-112">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cf9a4-113">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cf9a4-114">예제</span><span class="sxs-lookup"><span data-stu-id="cf9a4-114">EXAMPLES</span></span>

### <span data-ttu-id="cf9a4-115">예제 1: 통합 계정 계약 업데이트</span><span class="sxs-lookup"><span data-stu-id="cf9a4-115">Example 1: Update an integration account agreement</span></span>
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

<span data-ttu-id="cf9a4-116">이 명령은 지정된 Azure 리소스 그룹에서 통합 계정 계약을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="cf9a4-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="cf9a4-117">Example 2</span></span>

<span data-ttu-id="cf9a4-118">통합 계정 계약을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="cf9a4-119">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="cf9a4-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="cf9a4-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cf9a4-120">PARAMETERS</span></span>

### <span data-ttu-id="cf9a4-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="cf9a4-121">-AgreementContent</span></span>
<span data-ttu-id="cf9a4-122">계약에 대한 JSON(JavaScript 개체 표기) 형식으로 계약 내용을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="cf9a4-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="cf9a4-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="cf9a4-124">계약에 대한 계약 내용의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="cf9a4-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="cf9a4-125">-AgreementName</span></span>
<span data-ttu-id="cf9a4-126">통합 계정 계약의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="cf9a4-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="cf9a4-127">-AgreementType</span></span>
<span data-ttu-id="cf9a4-128">통합 계정 계약 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="cf9a4-129">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf9a4-130">X12</span><span class="sxs-lookup"><span data-stu-id="cf9a4-130">X12</span></span> 
- <span data-ttu-id="cf9a4-131">AS2</span><span class="sxs-lookup"><span data-stu-id="cf9a4-131">AS2</span></span>
- <span data-ttu-id="cf9a4-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="cf9a4-132">Edifact</span></span>

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

### <span data-ttu-id="cf9a4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9a4-133">-DefaultProfile</span></span>
<span data-ttu-id="cf9a4-134">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cf9a4-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf9a4-135">-Force</span><span class="sxs-lookup"><span data-stu-id="cf9a4-135">-Force</span></span>
<span data-ttu-id="cf9a4-136">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf9a4-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="cf9a4-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="cf9a4-138">게스트 파트너에 대한 이름 비즈니스 ID 한정자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="cf9a4-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="cf9a4-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="cf9a4-140">통합 계정 계약 게스트 ID 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="cf9a4-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="cf9a4-141">-GuestPartner</span></span>
<span data-ttu-id="cf9a4-142">게스트 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="cf9a4-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="cf9a4-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="cf9a4-144">호스트 파트너에 대한 이름 비즈니스 ID 한정자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="cf9a4-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="cf9a4-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="cf9a4-146">통합 계정 계약 호스트 ID 한정자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="cf9a4-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="cf9a4-147">-HostPartner</span></span>
<span data-ttu-id="cf9a4-148">호스트 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="cf9a4-149">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="cf9a4-149">-Metadata</span></span>
<span data-ttu-id="cf9a4-150">계약에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="cf9a4-151">-Name</span><span class="sxs-lookup"><span data-stu-id="cf9a4-151">-Name</span></span>
<span data-ttu-id="cf9a4-152">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cf9a4-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf9a4-153">-ResourceGroupName</span></span>
<span data-ttu-id="cf9a4-154">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cf9a4-155">-확인</span><span class="sxs-lookup"><span data-stu-id="cf9a4-155">-Confirm</span></span>
<span data-ttu-id="cf9a4-156">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf9a4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf9a4-157">-WhatIf</span></span>
<span data-ttu-id="cf9a4-158">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf9a4-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf9a4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9a4-160">CommonParameters</span></span>
<span data-ttu-id="cf9a4-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9a4-162">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf9a4-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9a4-163">입력</span><span class="sxs-lookup"><span data-stu-id="cf9a4-163">INPUTS</span></span>

### <span data-ttu-id="cf9a4-164">System.String</span><span class="sxs-lookup"><span data-stu-id="cf9a4-164">System.String</span></span>

## <span data-ttu-id="cf9a4-165">출력</span><span class="sxs-lookup"><span data-stu-id="cf9a4-165">OUTPUTS</span></span>

### <span data-ttu-id="cf9a4-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf9a4-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="cf9a4-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf9a4-167">NOTES</span></span>

## <span data-ttu-id="cf9a4-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf9a4-168">RELATED LINKS</span></span>

[<span data-ttu-id="cf9a4-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf9a4-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cf9a4-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf9a4-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cf9a4-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cf9a4-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


