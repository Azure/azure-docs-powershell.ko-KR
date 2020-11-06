---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: c825e77706a3f7efba3efac1e29866a8a296464b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527520"
---
# <span data-ttu-id="5f9d0-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5f9d0-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="5f9d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9d0-103">통합 계정 계약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f9d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f9d0-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f9d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f9d0-105">DESCRIPTION</span></span>
<span data-ttu-id="5f9d0-106">**AzureRmIntegrationAccountAgreement** Cmdlet은 Azure 리소스 그룹의 통합 계정 계약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="5f9d0-107">통합 계정 이름, 리소스 그룹 이름 및 규약 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="5f9d0-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5f9d0-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5f9d0-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5f9d0-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5f9d0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5f9d0-112">EXAMPLES</span></span>

### <span data-ttu-id="5f9d0-113">예제 1: 통합 계정 계약 받기</span><span class="sxs-lookup"><span data-stu-id="5f9d0-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="5f9d0-114">이 명령은 IntegrationAccountAgreement06 이라는 통합 계정 계약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="5f9d0-115">예제 2: 리소스 그룹 이름을 기준으로 통합 계정 계약 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f9d0-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="5f9d0-116">이 명령은 리소스 그룹 이름별 통합 계정 계약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="5f9d0-117">변수</span><span class="sxs-lookup"><span data-stu-id="5f9d0-117">PARAMETERS</span></span>

### <span data-ttu-id="5f9d0-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="5f9d0-118">-AgreementName</span></span>
<span data-ttu-id="5f9d0-119">통합 계정 계약의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="5f9d0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="5f9d0-120">-Name</span></span>
<span data-ttu-id="5f9d0-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5f9d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f9d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f9d0-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5f9d0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9d0-124">-DefaultProfile</span></span>
<span data-ttu-id="5f9d0-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f9d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9d0-126">CommonParameters</span></span>
<span data-ttu-id="5f9d0-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9d0-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f9d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9d0-129">입력</span><span class="sxs-lookup"><span data-stu-id="5f9d0-129">INPUTS</span></span>

## <span data-ttu-id="5f9d0-130">출력</span><span class="sxs-lookup"><span data-stu-id="5f9d0-130">OUTPUTS</span></span>

### <span data-ttu-id="5f9d0-131">IntegrationAccountAgreement를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="5f9d0-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="5f9d0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5f9d0-132">NOTES</span></span>

## <span data-ttu-id="5f9d0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f9d0-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f9d0-134">새로운 AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5f9d0-134">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="5f9d0-135">제거-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5f9d0-135">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="5f9d0-136">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5f9d0-136">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


