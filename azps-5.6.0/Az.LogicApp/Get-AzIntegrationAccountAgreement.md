---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 9ff2858eb032ff4ff4cc78e803b15f385fc71b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015088"
---
# <span data-ttu-id="642f3-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="642f3-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="642f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="642f3-102">SYNOPSIS</span></span>
<span data-ttu-id="642f3-103">통합 계정 계약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="642f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="642f3-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="642f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="642f3-105">DESCRIPTION</span></span>
<span data-ttu-id="642f3-106">**Get-AzIntegrationAccountAgreement** cmdlet은 Azure 리소스 그룹에서 통합 계정 계약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="642f3-107">통합 계정 이름, 리소스 그룹 이름 및 계약 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="642f3-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="642f3-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="642f3-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="642f3-111">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="642f3-112">예제</span><span class="sxs-lookup"><span data-stu-id="642f3-112">EXAMPLES</span></span>

### <span data-ttu-id="642f3-113">예제 1: 통합 계정 계약을 하세요.</span><span class="sxs-lookup"><span data-stu-id="642f3-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="642f3-114">이 명령은 IntegrationAccountAgreement06이라는 통합 계정 계약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="642f3-115">예제 2: 리소스 그룹 이름으로 통합 계정 계약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="642f3-116">이 명령은 리소스 그룹 이름으로 통합 계정 계약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="642f3-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="642f3-117">PARAMETERS</span></span>

### <span data-ttu-id="642f3-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="642f3-118">-AgreementName</span></span>
<span data-ttu-id="642f3-119">통합 계정 계약의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="642f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642f3-120">-DefaultProfile</span></span>
<span data-ttu-id="642f3-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="642f3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="642f3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="642f3-122">-Name</span></span>
<span data-ttu-id="642f3-123">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="642f3-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642f3-126">CommonParameters</span></span>
<span data-ttu-id="642f3-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="642f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642f3-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="642f3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642f3-129">입력</span><span class="sxs-lookup"><span data-stu-id="642f3-129">INPUTS</span></span>

### <span data-ttu-id="642f3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="642f3-130">System.String</span></span>

## <span data-ttu-id="642f3-131">출력</span><span class="sxs-lookup"><span data-stu-id="642f3-131">OUTPUTS</span></span>

### <span data-ttu-id="642f3-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="642f3-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="642f3-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="642f3-133">NOTES</span></span>

## <span data-ttu-id="642f3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="642f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="642f3-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="642f3-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="642f3-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="642f3-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="642f3-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="642f3-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


